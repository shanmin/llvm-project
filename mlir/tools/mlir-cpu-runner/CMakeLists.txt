set(LLVM_LINK_COMPONENTS
  Core
  Support
  nativecodegen
  native
  )

add_llvm_tool(mlir-cpu-runner
  mlir-cpu-runner.cpp
  )
llvm_update_compile_flags(mlir-cpu-runner)
target_link_libraries(mlir-cpu-runner PRIVATE
  MLIRAnalysis
  MLIREDSC
  MLIRExecutionEngine
  MLIRIR
  MLIRJitRunner
  MLIRLLVMIR
  MLIRLLVMToLLVMIRTranslation
  MLIROpenMP
  MLIROpenMPToLLVMIRTranslation
  MLIRParser
  MLIRTargetLLVMIRExport
  MLIRSupport
  )

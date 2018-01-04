Usage for each port:
1. Generate a FIFO for Rx data. Specify a data type of U16. Specify the write to never arbitrate.
2. Generate a FIFO for Rx health and status. Specify a data type of HealthAndStatusUpdate.ctl. Specify never arbitrate for write and read.
3. Generate a FIFO for Tx data. Specify a data type of U16. Specify never arbitrate for read.
4. Generate a FIFO for Tx health and status. Specify a data type of HealthAndStatusUpdate.ctl. Specify never arbitrate for write and read.
5. Generate a FIFO for Tx timestamps. Specify a data type of U64. Specify never arbitrate for write and read.
6. Drop the FPGAModbus/ModbusPort.vi onto your main VI. Setup the port settings using the resources defined above. Review the comments in ModbusPort.vi for more information.
7. Drop the FPGAHealthAndStatus/HealthAndStatusFIFOCopy.vi. Set the internal health and status FIFO. Set the source as the FIFO generated in step 2.
8. Drop the FPGAHealthAndStatus/HealthAndStatusFIFOCopy.vi. Set the internal health and status FIFO. Set the source as the FIFO generated in step 4.
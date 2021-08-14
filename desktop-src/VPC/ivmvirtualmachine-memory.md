---
title: Proprietà IVMVirtualMachine Memory (VPCCOMInterfaces.h)
description: Quantità di memoria fisica nella macchina virtuale, in megabyte.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Proprietà Memory Virtual PC
- Proprietà Memory Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Memory
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a828dde1804e546c97fe7cd2c161fc45366d416ba0e44900816c7bbee4b1ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344665"
---
# <a name="ivmvirtualmachinememory-property"></a>Proprietà IVMVirtualMachine::Memory

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta la quantità di memoria fisica nella macchina virtuale, in megabyte.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Valore proprietà

Specifica la quantità di memoria fisica, in megabyte.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                         | Significato                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>                  |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>              | Il parametro è **NULL.**<br/>                     |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>           | Il parametro non è valido o non è compreso nell'intervallo.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>      | La configurazione è sconosciuta.<br/>                  |
| <dl> <dt>Macchina virtuale \_ E \_ PREF \_ NOT \_ FOUND</dt> <dt>0xA0040300</dt> </dl> | La preferenza non è stata trovata.<br/>                  |
| <dl> <dt>Macchina virtuale \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | La macchina virtuale è in esecuzione o salvata.<br/>       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Si è verificato un errore imprevisto.<br/>              |



## <a name="remarks"></a>Commenti

La quantità di memoria fisica in una macchina virtuale deve essere di almeno 4 MB. Il limite massimo per la memoria dipende dalla configurazione host, ma può essere al massimo 3.712 MB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 


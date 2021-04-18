---
title: Proprietà Memory IVMVirtualMachine (VPCCOMInterfaces. h)
description: Quantità di memoria fisica della macchina virtuale, in megabyte.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Proprietà memoria Virtual PC
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
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300925"
---
# <a name="ivmvirtualmachinememory-property"></a>Proprietà IVMVirtualMachine:: memory

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>              | Il parametro è **null**.<br/>                     |
| <dl> <dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG </dl>           | Il parametro non è valido o non è compreso nell'intervallo.<br/> |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>      | La configurazione è sconosciuta.<br/>                  |
| <dl> <dt>Macchina virtuale \_ E \_ pref \_ non \_ trovato</dt> <dt>0xA0040300</dt> </dl> | La preferenza non è stata trovata.<br/>                  |
| <dl> <dt>Macchina virtuale \_ 0xA0040302 \_ virtuale E pref \_ VM \_ attiva</dt> <dt></dt> </dl> | La macchina virtuale è in esecuzione o salvata.<br/>       |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>      | Si è verificato un errore imprevisto.<br/>              |



## <a name="remarks"></a>Commenti

La quantità di memoria fisica in una macchina virtuale deve essere almeno 4 MB. Il limite superiore per la memoria dipende dalla configurazione host, ma può contenere al massimo 3.712 MB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 


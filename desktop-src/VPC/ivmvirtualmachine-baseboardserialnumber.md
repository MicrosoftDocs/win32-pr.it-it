---
title: Proprietà IVMVirtualMachine BaseBoardSerialNumber (VPCCOMInterfaces. h)
description: Numero di serie della lavagna di base.
ms.assetid: 374ad471-e0de-4e55-bab6-f7ddf3e5797f
keywords:
- Proprietà BaseBoardSerialNumber Virtual PC
- Proprietà BaseBoardSerialNumber Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà BaseBoardSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BaseBoardSerialNumber
- IVMVirtualMachine.get_BaseBoardSerialNumber
- IVMVirtualMachine.put_BaseBoardSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a6e239216eb5eadd492cb0a021d9f9c69610342
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400200"
---
# <a name="ivmvirtualmachinebaseboardserialnumber-property"></a>Proprietà IVMVirtualMachine:: BaseBoardSerialNumber

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e imposta il numero di serie della lavagna di base.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BaseBoardSerialNumber(
  [in]          BSTR baseBoardSerialNumber
);

HRESULT get_BaseBoardSerialNumber(
  [out, retval] BSTR *baseBoardSerialNumber
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il numero di serie della lavagna di base.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                               | Significato                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                                               |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                    | Il parametro è **null**.<br/>                                                  |
| <dl> <dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG </dl>                 | Il parametro è maggiore di 32 caratteri, una stringa vuota o non valido.<br/> |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>            | La configurazione è sconosciuta.<br/>                                               |
| <dl> <dt>Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata</dt> <dt>0xA004020B</dt> </dl> | Lo stato della macchina virtuale è in esecuzione o salvato.<br/>                         |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>            | Si è verificato un errore imprevisto.<br/>                                           |



## <a name="remarks"></a>Commenti

Questa proprietà non conterrà informazioni valide fino a quando la macchina virtuale non viene avviata per la prima volta. Se viene letta prima dell'avvio iniziale, verrà restituita una stringa vuota.

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

 


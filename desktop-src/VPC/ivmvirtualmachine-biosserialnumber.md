---
title: Proprietà IVMVirtualMachine BIOSSerialNumber (VPCCOMInterfaces.h)
description: Numero di serie del BIOS.
ms.assetid: a105009d-1c44-4079-a7d4-103cb02bad71
keywords:
- PROPRIETÀ BIOSSerialNumber Virtual PC
- Proprietà BIOSSerialNumber Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC , proprietà BIOSSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSSerialNumber
- IVMVirtualMachine.get_BIOSSerialNumber
- IVMVirtualMachine.put_BIOSSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f5cbf848f35cda387b1f596e68a7316e99cc7392c2c8c93c806186b961b37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123181"
---
# <a name="ivmvirtualmachinebiosserialnumber-property"></a>Proprietà IVMVirtualMachine::BIOSSerialNumber

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta il numero di serie del BIOS.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BIOSSerialNumber(
  [in]          BSTR biosSerialNumber
);

HRESULT get_BIOSSerialNumber(
  [out, retval] BSTR *biosSerialNumber
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il numero di serie del BIOS.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                               | Significato                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                                               |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                    | Il parametro è **NULL.**<br/>                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | Il parametro è maggiore di 32 caratteri, una stringa vuota o non è valido.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>            | La configurazione è sconosciuta.<br/>                                               |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE IN ESECUZIONE O SALVATA \_ \_ \_ 0XA004020B</dt> <dt></dt> </dl> | Lo stato della macchina virtuale è in esecuzione o salvato.<br/>                         |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                                           |



## <a name="remarks"></a>Commenti

Questa proprietà conterrà informazioni valide solo dopo l'avvio della macchina virtuale per la prima volta. Se viene letta prima dell'avvio iniziale, verrà restituita una stringa vuota.

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

 


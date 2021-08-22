---
title: Metodo IVMVirtualMachine DiscardUndoDisks (VPCCOMInterfaces.h)
description: Rimuove i dischi di annullamento virtuale.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- Metodo DiscardUndoDisks Virtual PC
- Metodo DiscardUndoDisks Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo DiscardUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997019bf25b4bcc37266c1ba39d5b1420ae44b800127f3e91bc5d9fcb4b76691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471943"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a>Metodo IVMVirtualMachine::D iscardUndoDisks

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rimuove i dischi di annullamento virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>            | La configurazione è sconosciuta.<br/>                                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE IN ESECUZIONE O SALVATA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl> | I dischi di annullamento virtuale non possono essere eliminati mentre la macchina virtuale è in esecuzione o in uno stato salvato.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                                                                    |



 

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

 


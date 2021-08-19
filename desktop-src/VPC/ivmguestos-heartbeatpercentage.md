---
title: Proprietà IVMGuestOS HeartbeatPercentage (VPCCOMInterfaces.h)
description: Percentuale di heartbeat previsti ricevuti negli ultimi minuti.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Proprietà HeartbeatPercentage Virtual PC
- Proprietà HeartbeatPercentage Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1415b9d59e28e5658dc5b54a1a6d118e0b12a77b3208978448afb2b336f313e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753448"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>Proprietà IVMGuestOS::HeartbeatPercentage

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la percentuale di heartbeat previsti ricevuti negli ultimi minuti.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>Valore proprietà

Percentuale di heartbeat previsti ricevuti nell'ultimo minuto.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                              | Significato                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'operazione è stata completata.<br/>                                                                                                            |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                   | Il parametro è **NULL.**<br/>                                                                                                               |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>           | La configurazione è sconosciuta.<br/>                                                                                                            |
| <dl> <dt>Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>      | Per questa operazione, la macchina virtuale deve essere in esecuzione.<br/>                                                                             |
| <dl> <dt>Macchina virtuale \_ E \_ ADDITIONS \_ NOT \_ AVAIL</dt> <dt>0xA0040504</dt> </dl> | La macchina virtuale non è completamente avviato, la funzionalità dei componenti di integrazione non è installata o la versione installata non supporta questa funzionalità.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Si è verificato un errore imprevisto.<br/>                                                                                                        |



## <a name="remarks"></a>Commenti

I componenti di integrazione invieranno un heartbeat periodico Windows pc virtuale mentre il sistema operativo guest è in esecuzione. Se il sistema operativo guest è molto caricato, è possibile che Windows Virtual PC riceva meno heartbeat del previsto. Se la percentuale di heartbeat scende a zero, è possibile che il sistema operativo guest non risponda o si arresti in modo anomalo. La macchina virtuale deve essere in esecuzione( ovvero completamente avviato e non arrestato) e i componenti di integrazione devono essere installati quando questa proprietà viene richiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS è definito come \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 


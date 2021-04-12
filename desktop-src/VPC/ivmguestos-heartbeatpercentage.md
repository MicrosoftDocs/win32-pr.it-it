---
title: Proprietà IVMGuestOS HeartbeatPercentage (VPCCOMInterfaces. h)
description: Percentuale di heartbeat previsti ricevuti nel minuto precedente.
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
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518801"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>Proprietà IVMGuestOS:: HeartbeatPercentage

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la percentuale di heartbeat previsti ricevuti nel minuto precedente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>Valore proprietà

Percentuale di heartbeat previsti ricevuti nel minuto precedente.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                              | Significato                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'operazione è stata completata.<br/>                                                                                                            |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                   | Il parametro è **null**.<br/>                                                                                                               |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>           | La configurazione è sconosciuta.<br/>                                                                                                            |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>      | Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.<br/>                                                                             |
| <dl> <dt>Macchina virtuale \_ \_Aggiunte di E \_ non \_ disponibili</dt> <dt>0xA0040504</dt> </dl> | La macchina virtuale non è stata avviata completamente, la funzionalità componenti di integrazione non è installata oppure la versione installata non supporta questa funzionalità.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>           | Si è verificato un errore imprevisto.<br/>                                                                                                        |



## <a name="remarks"></a>Commenti

I componenti di integrazione invieranno un heartbeat periodico a Windows Virtual PC mentre è in esecuzione il sistema operativo guest. Se il sistema operativo guest è caricato in modo elevato, è possibile che Windows Virtual PC riceva un minor numero di heartbeat del previsto. Se la percentuale di heartbeat scende a zero, è possibile che il sistema operativo guest non risponda o venga arrestato in modo anomalo. La macchina virtuale deve essere in esecuzione (ovvero completamente avviata e non arrestata) e i componenti di integrazione devono essere installati quando questa proprietà viene richiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 


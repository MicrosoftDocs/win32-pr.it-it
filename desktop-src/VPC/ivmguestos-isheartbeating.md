---
title: Proprietà IVMGuestOS IsInterfacebeating (VPCCOMInterfaces.h)
description: Determina se la macchina virtuale ha un heartbeat.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Proprietà IsAting Virtual PC
- Proprietà IsAting Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà Is Facile da utilizzare
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91598284d3765c5ff6de185ca0cf3b652036c226d80b0fe01a9944a9d7480b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594181"
---
# <a name="ivmguestosisheartbeating-property"></a>Proprietà IVMGuestOS::Is Libeating

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina se la macchina virtuale ha un heartbeat.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Valore proprietà

**VARIANT \_ TRUE** se viene rilevato un heartbeat, **VARIANT FALSE in \_ caso** contrario.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                              | Significato                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'operazione è stata completata.<br/>                                                                                                                         |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                   | Il parametro è **NULL.**<br/>                                                                                                                            |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>           | La configurazione è sconosciuta.<br/>                                                                                                                         |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl>      | La macchina virtuale deve essere in esecuzione per questa operazione.<br/>                                                                                               |
| <dl> <dt>Macchina virtuale \_ E \_ ADDITIONS \_ NOT \_ AVAIL</dt> <dt>0xA0040504</dt> </dl> | La macchina virtuale non è completamente avviata, la funzionalità dei componenti di integrazione non è installata o la versione installata non supporta questa funzionalità.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>           | Si è verificato un errore imprevisto.<br/>                                                                                                                     |



## <a name="remarks"></a>Commenti

Quando i componenti di integrazione vengono installati nel sistema operativo guest, viene inviato un normale "tick" o heartbeat dalla sessione della macchina virtuale Windows Virtual PC. Se il sistema operativo guest è molto caricato, è possibile che Virtual PC riceva meno heartbeat del previsto. Se non viene rilevato alcun heartbeat, è possibile che il sistema operativo guest non risponda o si arresti in modo anomalo.

Per impostazione predefinita, una macchina virtuale produce dieci tick di heartbeat al minuto. Se non vengono rilevati tick di heartbeat per un intero minuto, Windows Virtual PC tenterà di riavviare la sessione della macchina virtuale una volta ogni dieci secondi per un massimo di due minuti. Questo comportamento è controllato dai valori chiave seguenti nel file di configurazione della sessione della macchina virtuale.



| Chiave di configurazione                                            | Predefinito       | Descrizione                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| integration/microsoft/heartbeat/time<br/>              | 60<br/> | Durata, in secondi, del blocco di tempo utilizzato per generare i tick di heartbeat.<br/>                                             |
| integration/microsoft/heartbeat/rate<br/>              | 10<br/> | Numero di tick generati in ogni blocco di tempo heartbeat.<br/>                                                                  |
| integration/microsoft/heartbeat/failure \_ interval<br/> | 10<br/> | Numero di secondi tra i tentativi di riavvio, quando non vengono ricevuti tick di heartbeat all'interno di un blocco di tempo heartbeat specifico.<br/> |
| integration/microsoft/heartbeat/failure \_ attempts<br/> | 12<br/> | Numero di tentativi di riavvio effettuati.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 


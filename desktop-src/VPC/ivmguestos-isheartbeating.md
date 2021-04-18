---
title: Proprietà di heartbeat IVMGuestOS (VPCCOMInterfaces. h)
description: Determina se la macchina virtuale ha un heartbeat.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Proprietà di heartbeat-PC virtuale
- Proprietà di heartbeat, Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà di heartbeat
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
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302562"
---
# <a name="ivmguestosisheartbeating-property"></a>Proprietà IVMGuestOS:: heartbeat

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se la macchina virtuale ha un heartbeat.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Valore proprietà

**Variante \_ TRUE** se viene rilevato un heartbeat, **Variant \_ false** in caso contrario.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                              | Significato                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'operazione è stata completata.<br/>                                                                                                                         |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                   | Il parametro è **null**.<br/>                                                                                                                            |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>           | La configurazione è sconosciuta.<br/>                                                                                                                         |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>      | Per questa operazione è necessario che la macchina virtuale sia in esecuzione.<br/>                                                                                               |
| <dl> <dt>Macchina virtuale \_ \_Aggiunte di E \_ non \_ disponibili</dt> <dt>0xA0040504</dt> </dl> | La macchina virtuale non è stata avviata completamente, la funzionalità componenti di integrazione non è installata oppure la versione installata non supporta questa funzionalità.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>           | Si è verificato un errore imprevisto.<br/>                                                                                                                     |



## <a name="remarks"></a>Commenti

Quando si installano componenti di integrazione nel sistema operativo guest, viene inviato un normale "battito" o un heartbeat dalla sessione della macchina virtuale a Windows Virtual PC. Se il sistema operativo guest è caricato in modo elevato, è possibile che Virtual PC riceva un minor numero di heartbeat del previsto. Se non viene rilevato alcun heartbeat, è possibile che il sistema operativo guest non risponda o venga arrestato in modo anomalo.

Per impostazione predefinita, una macchina virtuale produce dieci cicli di heartbeat al minuto. Se non viene rilevato alcun battito di heartbeat per un minuto intero, Windows Virtual PC tenterà di riavviare la sessione della macchina virtuale una volta ogni dieci secondi per un massimo di due minuti. Questo comportamento è controllato dai valori chiave seguenti nel file di configurazione della sessione della macchina virtuale.



| Chiave di configurazione                                            | Predefinito       | Descrizione                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| integrazione/Microsoft/heartbeat/ora<br/>              | 60<br/> | Lunghezza del blocco di tempo utilizzato per generare i cicli di heartbeat, in secondi.<br/>                                             |
| integrazione/Microsoft/heartbeat/frequenza<br/>              | 10<br/> | Numero di cicli generati in ogni blocco di tempo heartbeat.<br/>                                                                  |
| integrazione/Microsoft/heartbeat/intervallo di errori \_<br/> | 10<br/> | Il numero di secondi tra i tentativi di riavvio, quando non viene ricevuto alcun battito di heartbeat entro un blocco di tempo heartbeat specifico.<br/> |
| tentativi di integrazione/Microsoft/heartbeat/errore \_<br/> | 12<br/> | Numero di tentativi di riavvio effettuati.<br/>                                                                                         |



 

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

 


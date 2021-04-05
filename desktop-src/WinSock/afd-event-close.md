---
description: Evento di traccia di rete Winsock per l'operazione di chiusura del socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: Evento AFD_EVENT_CLOSE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751487"
---
# <a name="afd_event_close-event"></a>\_Evento di \_ chiusura evento AFD

L'evento di **\_ \_ chiusura evento AFD** è un evento di traccia di rete Winsock per l'operazione di chiusura del socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informazioni su questo evento.

Nella tabella seguente sono elencati i valori possibili per il parametro *EnterExit* :



| Valore                                                                        | Significato                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inizio di una richiesta Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | La richiesta Winsock è stata completata.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Il driver AFD Winsock ha intrapreso un'azione interna (ad esempio, l'interruzione di una connessione).<br/>      |
| <dl> <dt>3</dt> </dl> | Questo evento è stato generato dal driver TCP/IP. Questo indica in genere una notifica dei dati.<br/> |
| <dl> <dt>4</dt> </dl> | Il driver AFD Winsock ha causato il verificarsi di questo evento (ad esempio, l'impostazione di un'opzione socket).<br/> |



 

</dd> <dt>

*Posizione* 
</dt> <dd>

Campo privato utilizzato internamente.

</dd> <dt>

*Processo* 
</dt> <dd>

Indirizzo [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del processo a cui appartiene il socket correlato. Si tratta di una struttura opaca che funge da oggetto processo per un processo. Per ulteriori informazioni, vedere la documentazione del kit driver Windows per la struttura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Endpoint* 
</dt> <dd>

Indirizzo dell' \_ endpoint AFD del socket.

</dd> <dt>

*Status* 
</dt> <dd>

Codice NTSTATUS per l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento di **\_ \_ chiusura evento AFD** viene tracciato per un'operazione di rete Winsock per la chiusura di un socket. Il canale per questo evento è Winsock-AFD. Il livello per questo evento è informativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**\_descrittore evento**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 


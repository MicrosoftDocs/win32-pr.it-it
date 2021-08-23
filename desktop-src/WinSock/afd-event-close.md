---
description: Evento di traccia di rete Winsock per l'operazione di chiusura del socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE evento
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
ms.openlocfilehash: 9068809c052638e33d45a5affadc23a289fa65ae04e6b1a71af1e40e4b508b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993751"
---
# <a name="afd_event_close-event"></a>Evento AFD \_ EVENT \_ CLOSE

**L'evento AFD \_ EVENT CLOSE \_ è** un evento di traccia di rete Winsock per l'operazione di chiusura del socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informazioni su questo evento.

Nella tabella seguente sono elencati i valori possibili per *il parametro EnterExit:*



| Valore                                                                        | Significato                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inizio di una richiesta Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Richiesta Winsock completata.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Il driver Winsock AFD ha seguito un'azione interna, ad esempio l'interruzione di una connessione.<br/>      |
| <dl> <dt>3</dt> </dl> | Il driver TCP/IP ha causato il verificarsi di questo evento. Ciò indica in genere una notifica dei dati.<br/> |
| <dl> <dt>4</dt> </dl> | Il driver Winsock AFD ha causato il verificarsi di questo evento (ad esempio, l'impostazione di un'opzione socket).<br/> |



 

</dd> <dt>

*Posizione* 
</dt> <dd>

Campo privato utilizzato internamente.

</dd> <dt>

*Processo* 
</dt> <dd>

Indirizzo [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del processo proprietario del socket correlato. Si tratta di una struttura opaca che funge da oggetto processo per un processo. Per altre informazioni, vedere la documentazione Windows Driver Kit per la [struttura EPROCESS.](/windows-hardware/drivers/kernel/eprocess)

</dd> <dt>

*Endpoint* 
</dt> <dd>

Indirizzo ENDPOINT AFD \_ del socket.

</dd> <dt>

*Status* 
</dt> <dd>

Codice NTSTATUS per l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'evento \_ AFD EVENT \_ CLOSE** viene tracciato per un'operazione di rete Winsock per chiudere un socket. Il canale per questo evento è Winsock-AFD. Il livello di questo evento è informativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della traccia winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**DESCRITTORE \_ DI EVENTI**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia di Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli traccia modifiche catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 


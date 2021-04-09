---
title: Classe MSAD_ReplNeighbor
description: Rappresenta la \_ \_ struttura Neighbor REPL di DS, che contiene le informazioni sullo stato di replica in ingresso per un particolare contesto dei nomi (NC) e una coppia di server di origine.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- Classe MSAD_ReplNeighbor Active Directory
- Classe MSAD_ReplNeighbor Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964264"
---
# <a name="msad_replneighbor-class"></a>\_Classe MSAD ReplNeighbor

Rappresenta la [**struttura \_ \_ Neighbor REPL di DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) , che contiene le informazioni sullo stato di replica in ingresso per una determinata coppia di contesto dei nomi e server di origine, come restituito dalla funzione [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a>Members

La **classe \_ ReplNeighbor di MSAD** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ ReplNeighbor di MSAD** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**SyncNamingContext**](syncnamingcontext-msad-replneighbor.md) | Sincronizza un contesto dei nomi di destinazione con una delle relative origini.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ ReplNeighbor di MSAD** dispone di queste proprietà.

<dl> <dt>

**AsyncIntersiteTransportDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X. 500 dell'oggetto [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) che corrisponde al trasporto su cui viene eseguita la replica. Impostare su **null** per la replica RPC/IP.

</dd> <dt>

**AsyncIntersiteTransportObjGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il GUID dell'oggetto trasporto tra siti che corrisponde alla proprietà **AsyncIntersiteTransportDN** .

</dd> <dt>

**CompressChanges**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ compress \_ changes** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**DisableScheduledSync**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ sincronizzazione pianificata per la disabilitazione di DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome canonico del dominio del NC replicato.

</dd> <dt>

**DoScheduledSyncs**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ sincronizzazione pianificato DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**FullSyncInProgress**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il **flag \_ \_ \_ \_ \_ di sincronizzazione \_ completa DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**FullSyncNextPacket**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag del **\_ \_ \_ \_ \_ \_ pacchetto successivo DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**IgnoreChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag di **notifica delle \_ \_ \_ \_ modifiche \_ di DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**IsDeletedSourceDsa**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se questa connessione rappresenta un controller di dominio di origine che è stato eliminato. **True** se questa connessione rappresenta un controller di dominio di origine che è stato eliminato. in caso contrario, **false**. Per impostazione predefinita, il servizio DS continuerà a replicare queste connessioni per un certo periodo di tempo dopo l'eliminazione del controller di dominio di origine.

</dd> <dt>

**LastSyncResult**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il codice di errore **HRESULT** per l'ultimo tentativo di replica.

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il numero di tentativi consecutivi di replica non riusciti, escluse le connessioni che dovrebbero avere esito negativo. Se, ad esempio, la proprietà **IsDeletedSourceDsa** è impostata su **true**, è previsto che abbia esito negativo.

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il percorso X. 500 per il NC replicato da questa connessione.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il GUID per il NC replicato.

</dd> <dt>

**NeverSynced**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ mai \_ sincronizzato** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**NoChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ No \_ Change \_ Notifications** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**NumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il numero di tentativi consecutivi di replica non riusciti.

</dd> <dt>

**ReplicaFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il set di flag che specificano attributi e opzioni per i dati di replica. Questa proprietà può essere zero o una combinazione di uno o più dei flag seguenti.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ scrivibile** (16 (0x10))


</dt> <dd>

La copia locale del contesto di denominazione è modificabile.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Sync \_ all' \_ avvio** (32 (0x20))


</dt> <dd>

Viene eseguito un tentativo di replica del contesto dei nomi da questa origine quando viene avviato il server di destinazione. Questo flag in genere si applica solo agli elementi adiacenti all'interno del sito.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ do \_ \_ syncs scheduled** (64 (0x40))


</dt> <dd>

La replica viene eseguita in base a una pianificazione. Questo flag viene in genere impostato a meno che la pianificazione per questo contesto dei nomi o origine non sia "mai", ovvero la pianificazione vuota.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Usa \_ il \_ \_ trasporto asincrono tra siti** (128 (0x80))


</dt> <dd>

La replica viene eseguita indirettamente tramite il servizio Messaggistica tra siti (ISM). Questo flag è impostato solo per la replica tramite SMTP. Il flag non è impostato durante la replica tramite RPC/IP tra siti.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ \_ bidirezionale \_ Sync** (512 (0x200))


</dt> <dd>

Se impostato, indica che quando la replica in ingresso è completa, il server di destinazione deve indicare al server di origine di eseguire la sincronizzazione in direzione inversa. Questa funzionalità viene utilizzata nel caso di connessioni remote, qualora solo uno dei due server sia in grado di inizializzare la connessione. Questa opzione, ad esempio, può essere usata in una sede aziendale e in una succursale, in cui la succursale si connette alla sede aziendale tramite Internet per mezzo di una connessione ISP remota.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Restituisci \_ oggetti \_ padre** (2048 (0x800))


</dt> <dd>

L'elemento adiacente restituisce gli oggetti padre prima degli oggetti figlio. Questo stato viene attivato quando l'elemento adiacente riceve un oggetto figlio prima del padre.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>Servizi di **dominio Active Directory \_ \_ \_ Sincronizzazione completa REPL \_ NBR \_ in \_ corso** (65536 (0x10000))


</dt> <dd>

È in corso una sincronizzazione completa del server di destinazione dal server di origine. Le sincronizzazioni complete non utilizzano vettori per la creazione di aggiornamenti (ad esempio, i [**\_ \_ cursori REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) per filtrare gli aggiornamenti. Le sincronizzazioni complete non vengono utilizzate come parte del protocollo di replica predefinito.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>Servizi di **dominio Active Directory \_ \_ \_ \_ \_ \_ Pacchetto successivo sincronizzazione completa REPL NBR** (131072 (0x20000))


</dt> <dd>

L'ultimo pacchetto dall'origine indica una modifica di un oggetto non ancora creato dal server di destinazione. Il pacchetto successivo da richiedere indica al server di origine di inserire tutti gli attributi dell'oggetto modificato nel pacchetto.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ mai \_ sincronizzato** (2097152 (0x200000))


</dt> <dd>

Non è mai stata completata alcuna operazione di sincronizzazione da questa origine.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR con \_ precedenza** (16777216 (0x1000000))


</dt> <dd>

Il motore di replica ha interrotto temporaneamente l'elaborazione di questo elemento adiacente per poter servire un altro Neighbor con priorità più alta, per questa partizione o per un'altra partizione. L'elaborazione dell'elemento adiacente verrà ripresa dal motore di replica una volta completato il lavoro con priorità più alta.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Ignora \_ le \_ notifiche di modifica** (67108864 (0x4000000))


</dt> <dd>

Questa adiacente è impostata per disabilitare le sincronizzazioni basate sulla notifica. All'interno di un sito, la sincronizzazione tra ciascun controller di dominio avviene in base alle notifiche inviate in caso di modifica. Questa impostazione impedisce al router adiacente di eseguire sincronizzazioni attivate da notifiche. Il router adiacente eseguirà comunque le sincronizzazioni in base alla pianificazione o in risposta alle sincronizzazioni richieste manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Disable \_ scheduled \_ Sync** (134217728 (0x8000000))


</dt> <dd>

Questo elemento adiacente è impostato in modo da non eseguire sincronizzazioni in base alla pianificazione. L'unico modo in cui il prossimo eseguirà le sincronizzazioni è in risposta alle notifiche di modifica o alle sincronizzazioni richieste manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>Servizi di **dominio Active Directory \_ \_ \_ \_ Modifiche REPL NBR Compress** (268435456 (0x10000000))


</dt> <dd>

Le modifiche ricevute da questa origine devono essere compresse. La compressione viene in genere eseguita solo se il server di origine si trova in un sito diverso.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ senza \_ \_ notifiche di modifica** (536870912 (0x20000000))


</dt> <dd>

Nessuna notifica delle modifiche deve essere ricevuta da questa origine. Viene in genere impostato solo se il server di origine si trova in un sito diverso.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>Servizi di **dominio Active Directory \_ \_Set di \_ \_ attributi \_ parziali REPL NBR** (1073741824 (0x40000000))


</dt> <dd>

È in corso la ricompilazione da parte dell'elemento adiacente del contenuto di questa replica, in seguito a una modifica nell'insieme di attributi parziali.

</dd> </dl>

</dd> <dt>

**SourceDsaAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'indirizzo DNS del controller di dominio di origine.

> [!Note]  
> Questa stringa contiene un GUID modificato, non il nome DNS canonico comunemente usato.

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il componente del percorso dell'oggetto per il DSA che rappresenta il controller di dominio di origine. Questa stringa è spesso simile al nome del computer, ma non è sempre identica.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X. 500 per il DSA che rappresenta il controller di dominio di origine.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'ID di chiamata utilizzato dal server di origine nell'ultima replica.

</dd> <dt>

**SourceDsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il GUID per l'agente del servizio directory (DSA) che rappresenta il controller di dominio di origine (DC).

</dd> <dt>

**SourceDsaSite**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il sito che contiene il controller di dominio di origine.

</dd> <dt>

**SyncOnStartup**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ Sync \_ on \_ Startup** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**TimeOfLastSyncAttempt**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp per l'ultimo tentativo di replica.

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il timestamp per l'ultimo tentativo di replica riuscito.

</dd> <dt>

**TwoWaySync**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ sincronizzazione bidirezionale DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**UseAsyncIntersiteTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ \_ trasporto tra siti DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore della proprietà **USNLastObjChangeSynced** alla fine dell'ultimo ciclo di replica completato correttamente. Zero se i cicli di replica non sono stati completati correttamente.

</dd> <dt>

**USNLastObjChangeSynced**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore dell'attributo non [**modificato**](/windows/desktop/ADSchema/a-usnchanged) dell'ultimo aggiornamento dell'oggetto ricevuto.

</dd> <dt>

**Scrivibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il **flag \_ scrivibile di DS REPL \_ NBR \_** è stato impostato nella proprietà **ReplicaFlags** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\MicrosoftActiveDirectory radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 


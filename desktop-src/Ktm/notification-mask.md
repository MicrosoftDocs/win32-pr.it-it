---
description: Elenca i diversi tipi di notifiche che possono essere ricevute da un'integrazione.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17391d2b406b3f7a3ee9a3a868bc1b6734050c787fdbb432785e5be0b917468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146544"
---
# <a name="notification_mask"></a>MASCHERA DI \_ NOTIFICA

Elenca i diversi tipi di notifiche che possono essere ricevute da un'integrazione.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**MASCHERA \_ DI NOTIFICA \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Maschera che indica tutti i bit validi per una notifica di transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**\_PREPREPARE NOTIFICA \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Questa notifica viene chiamata dopo che un client chiama [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) e nessun gestore delle risorse (RM) supporta il commit a fase singola o una gestione transazioni superiore (TM) chiama [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). Questa notifica viene ricevuta dalle macchine virtuali che indicano che devono completare qualsiasi operazione che potrebbe causare l'integrazione di altre macchine virtuali in una transazione, ad esempio lo scaricamento della cache. Dopo aver completato queste operazioni, RM deve chiamare [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Per ricevere questa notifica, RM deve supportare anche **TRANSACTION \_ NOTIFY \_ PREPARE** e **TRANSACTION NOTIFY \_ \_ COMMIT.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**PREPARAZIONE \_ DELLE NOTIFICHE DELLE \_ TRANSAZIONI**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Questa notifica viene chiamata al termine **dell'elaborazione TRANSACTION \_ NOTIFY \_ PREPREPARE.** Segnala al RM di completare tutte le operazioni associate all'integrazione, in modo da garantire che un'operazione di commit possa avere esito positivo e che un'operazione di interruzione possa avere esito positivo. In genere, la maggior parte del lavoro per una transazione viene eseguita durante la fase di preparazione. Per le macchine virtuali durevoli, è necessario registrare lo stato prima di chiamare la [**funzione PrepareComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) Si tratta dell'ultima possibilità che l'RM richiedi il rollback della transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**COMMIT \_ DI NOTIFICA \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Questa notifica segnala all'RM di completare tutte le operazioni associate all'integrazione. In genere, il RM rilascia eventuali blocchi, rilascia tutte le informazioni necessarie per eseguire il rollback della transazione. L'RM deve rispondere chiamando la [**funzione CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) al termine di queste operazioni.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION \_ NOTIFY \_ ROLLBACK**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Questa notifica segnala all'RM di annullare tutte le operazioni eseguite associate alla transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_PREPREPARE NOTIFICA \_ \_ TRANSAZIONE COMPLETATA**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di pre-preparazione è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**PREPARAZIONE \_ NOTIFICA \_ TRANSAZIONE \_ COMPLETATA**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di preparazione è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**COMMIT \_ DI NOTIFICA \_ \_ TRANSAZIONE COMPLETATO**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di commit è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**ROLLBACK \_ NOTIFICA \_ TRANSAZIONE \_ COMPLETATO**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di rollback è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**RECUPERO \_ NOTIFICA \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Questa notifica segnala alle macchine virtuali che devono recuperare il proprio stato perché è necessario ripristinare il risultato di una transazione. Ad esempio, quando un RM viene recuperato e quando sono presenti transazioni in dubbio. Questa notifica viene recapitata dopo la risoluzione dello stato in dubbio.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**COMMIT \_ A FASE SINGOLA DI NOTIFICA DELLA \_ \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Questa notifica segnala al RM di completare ed eseguire il commit della transazione senza usare un protocollo di commit in due fasi. Se il RM vuole usare un'operazione in due fasi, deve rispondere chiamando la [**funzione SinglePhaseReject.**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**COMMIT \_ DELEGATO DI NOTIFICA \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM segnala al TM superiore di eseguire un'operazione di commit.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**QUERY \_ DI RECUPERO NOTIFICA \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM segnala al TM superiore di eseguire query sullo stato di una transazione in dubbio.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_PREPREPARE PER \_ L'INTEGRAZIONE DI TRANSACTION \_ NOTIFY**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Questa notifica segnala al TM superiore che le notifiche di pre-preparazione devono essere recapitate nell'integrazione specificata.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION \_ NOTIFY \_ LAST \_ RECOVER**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Questa notifica indica che l'operazione di ripristino è stata completata per questo RM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION \_ NOTIFY \_ INDOUBT**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



La transazione specificata si trova in uno stato in dubbio. L'agente di gestione delle transazioni riceve questa notifica durante le operazioni di ripristino quando è stata preparata una transazione, ma non è disponibile alcun gestore delle transazioni superiore. Ad esempio, quando una transazione coinvolge un TM remoto e tale nodo non è disponibile, il relativo nodo non è disponibile o il servizio [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) locale non è disponibile, lo stato della transazione è in dubbio.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**NOTIFICA \_ DELLE \_ TRANSAZIONI TM \_ ONLINE**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



La TM è online e accetta richieste.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**RISULTATO \_ DELLA RICHIESTA DI NOTIFICA DELLA \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Segnala alle macchine virtuali che sono disponibili informazioni sui risultati e che deve essere effettuata una richiesta per queste informazioni.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**FINALIZZAZIONE \_ \_ COMMIT NOTIFICA \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Riservato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                            |
| Intestazione<br/>                   | <dl> <dt>KtmTypes.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Costanti di Gestione transazioni kernel](kernel-transaction-manager-constants.md)
</dt> <dt>

[**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**NOTIFICA DELLE \_ TRANSAZIONI**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 


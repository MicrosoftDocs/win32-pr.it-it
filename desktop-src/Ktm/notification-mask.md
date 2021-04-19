---
description: Elenca i diversi tipi di notifiche che possono essere ricevute da un elenco.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314799"
---
# <a name="notification_mask"></a>maschera di notifica \_

Elenca i diversi tipi di notifiche che possono essere ricevute da un elenco.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_maschera notifiche \_ transazione**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Maschera che indica tutti i bit validi per una notifica di transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**\_notifica \_ PREpreparazione transazione**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Questa notifica viene chiamata dopo che un client chiama [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) e nessun Resource Manager (RM) supporta il commit a fase singola o una gestione transazioni (TM) superiore chiama [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). Questa notifica viene ricevuta da RMs indicante che è necessario completare qualsiasi lavoro che potrebbe causare l'integrazione di altri RMs in una transazione, ad esempio lo svuotamento della cache. Al termine di queste operazioni, è necessario che RM chiami [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Per ricevere questa notifica, è necessario che RM supporti inoltre il **\_ \_ commit** della notifica **della transazione e \_ \_** della notifica della transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**notifica della transazione- \_ \_ prepara**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Questa notifica viene chiamata dopo il completamento dell'elaborazione della **\_ notifica \_** preliminare della transazione. Segnala a RM di completare tutte le operazioni associate a questa integrazione, in modo da garantire che un'operazione di commit possa avere esito positivo e che anche un'operazione di interruzione possa avere esito positivo. In genere, la maggior parte del lavoro per una transazione viene eseguita durante la fase di preparazione. Per RMs durevole, è necessario che registrino il proprio stato prima di chiamare la funzione [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) . Questa è l'ultima possibilità per l'RM di richiedere che venga eseguito il rollback della transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_commit notifica \_ transazione**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Questa notifica segnala a RM di completare tutte le operazioni associate a questa integrazione. In genere, RM rilascia tutti i blocchi, rilascia tutte le informazioni necessarie per eseguire il rollback della transazione. Il RM deve rispondere chiamando la funzione [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) al termine di queste operazioni.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**\_rollback notifiche \_ transazione**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Questa notifica segnala a RM di annullare tutte le operazioni eseguite associate alla transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_pre- \_ preparazione notifica transazioni \_ completata**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di pre-preparazione è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**\_preparazione notifica \_ transazioni \_ completata**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di preparazione è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**\_commit notifica \_ transazioni \_ completato**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di commit è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**\_rollback notifiche \_ transazioni \_ completato**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Questa notifica segnala al TM superiore che un'operazione di rollback è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_recupero notifiche \_ transazioni**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Questa notifica segnala a RMs che devono ripristinare il proprio stato perché è necessario recapitare il risultato di una transazione. Ad esempio, quando un RM viene recuperato e in caso di transazioni rimaste in dubbio. Questa notifica viene recapitata una volta risolto lo stato in dubbio.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**COMMIT di una \_ \_ singola \_ fase di notifica transazione \_**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Questa notifica segnala a RM di completare ed eseguire il commit della transazione senza utilizzare un protocollo di commit in due fasi. Se RM vuole usare un'operazione in due fasi, deve rispondere chiamando la funzione [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_commit del \_ delegato \_ Notify transazione**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM segnala alla TM superiore di eseguire un'operazione di commit.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_query di \_ recupero \_ notifica transazioni**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM segnala alla TM superiore di eseguire una query sullo stato di una transazione in dubbio.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_pre- \_ \_ preparazione della notifica della transazione**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Questa notifica segnala al TM superiore che le notifiche preliminari devono essere recapitate nell'elenco specificato.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ ultimo ripristino notifiche \_ transazioni**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Questa notifica indica che l'operazione di ripristino è stata completata per questo RM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**notifica di transazione \_ \_ indubbia**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Lo stato della transazione specificata è in dubbio. Il RM riceve questa notifica durante le operazioni di ripristino quando una transazione è stata preparata, ma non è disponibile una gestione transazioni superiore (TM). Ad esempio, quando una transazione include una TM remota e tale nodo non è disponibile, il nodo non è disponibile o il servizio [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) locale non è disponibile, lo stato della transazione è in dubbio.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**\_notifica transazioni \_ TM \_ online**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



TM è online e accetta le richieste.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_risultato della \_ richiesta di notifica della transazione \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Segnala a RMs che sono disponibili informazioni sul risultato e che è necessario effettuare una richiesta per tali informazioni.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_ \_ finalizzazione commit notifica transazione \_**
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
| Intestazione<br/>                   | <dl> <dt>KtmTypes. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Costanti di gestione transazioni kernel](kernel-transaction-manager-constants.md)
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

[**\_notifica transazioni**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 


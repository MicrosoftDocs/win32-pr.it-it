---
description: 'VSS consente la presenza di molte copie shadow in una sola volta, ma consente solo la creazione di un set di copie shadow in corso tra la chiamata a IVssBackupComponents:: StartSnapshotSet e la restituzione dalla chiamata a IVssBackupComponents::D oSnapshotSet.'
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Gestione degli errori nei provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f040526f63a0fe57fc5a49ac903e8b60b76646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318587"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Gestione degli errori nei provider di copie shadow

VSS consente la presenza di molte copie shadow in una sola volta, ma consente solo la creazione di un set di copie shadow in corso tra la chiamata a [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e la restituzione dalla chiamata a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).

## <a name="no-partial-commit"></a>Nessun commit parziale

Se un provider non riesce a eseguire una copia shadow su un volume o un LUN nel set di copie shadow, la creazione dell'intero set di copie shadow ha esito negativo. Questo si verifica per motivi strutturali. Questa progettazione semplifica i problemi comportamentali associati alla semantica degli errori parziali e mantiene un temporizzato coerente in tutte le copie shadow nel set.

## <a name="reporting-fault-conditions"></a>Segnalazione di condizioni di errore

Se si verifica un errore del provider o una condizione di errore, il provider deve registrare un errore nel registro eventi dell'applicazione. Sono inclusi, tra gli altri, gli eventuali errori specifici del provider durante la creazione o l'importazione di un set di copie shadow o un errore di allocazione delle risorse per la copia shadow di copia in scrittura dopo la creazione. Questa registrazione non deve essere eseguita nel momento in cui i volumi nel set di copie shadow sono in uno stato bloccato.

## <a name="valid-provider-return-values"></a>Valori restituiti del provider validi

Nella tabella seguente sono elencati i codici restituiti validi per i metodi del provider e i relativi significati.



| Valore                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>\_OK<br/>                                                                                                                     | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ OutOfMemory<br/>                                                                                          | Il provider ha esaurito la memoria o altre risorse di sistema.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | Uno dei valori di parametro non è valido.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ AccessDenied<br/>                                                                                       | Un client senza privilegi ha tentato di chiamare il provider.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>\_stato non \_ valido VSS E \_<br/>                                                                                  | Nessun provider supporta l'operazione richiesta oppure non è possibile eseguire l'operazione sull'oggetto perché lo stato dell'oggetto non è corretto.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>\_oggetto VSS \_ E \_ non \_ trovato<br/>                                                            | Un parametro fa riferimento a un oggetto non trovato, ad esempio un ID copia shadow, un ID set di copie shadow o un volume.<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>\_archiviazione VSS E \_ insufficiente \_<br/>                                                 | Il provider non è in grado di eseguire l'operazione perché lo spazio su disco è insufficiente.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>\_Volume VSS \_ E \_ non \_ supportato<br/>                                                | Nessun provider del computer supporta l'operazione richiesta nel volume.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>\_Volume VSS \_ E \_ non \_ supportato \_ dal \_ provider<br/>          | Il provider non supporta il volume.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>\_ \_ \_ numero massimo \_ di snapshot VSS E \_ \_ raggiunto<br/> | Il provider ha raggiunto il numero massimo di copie shadow che può supportare.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>\_veto del \_ provider VSS E \_<br/>                                                                      | Il provider ha rilevato un errore di run-time interno che non esegue il mapping a un altro valore restituito. Il provider deve inoltre scrivere un evento nel registro eventi dell'applicazione, fornendo all'utente informazioni su come risolvere il problema.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E \_ non è in grado di \_ ripristinare un \_ DiskID<br/>                                                | Impossibile impostare il valore richiesto per la firma MBR o l'ID GPT per uno o più dischi. Per ulteriori informazioni, consultare il registro eventi dell'applicazione.<br/>                                                                                            |



 

Il provider non deve tentare di restituire altri codici di errore.

Se il provider restituisce un codice di errore non previsto (ad esempio, **\_ false**, **e \_ Fail**, **e \_ Unexpected**, o **e \_ Abort**), VSS scrive un evento nel registro eventi che indica il provider e il metodo non riuscito e converte l'errore in VSS e il provider imprevisto **\_ \_ \_ \_ Error** prima di tornare al richiedente. Questa operazione non viene eseguita per qualsiasi risultato restituito da [**IVssProviderCreateSnapshotSet:: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) o [**IVssProviderNotifications:: OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 





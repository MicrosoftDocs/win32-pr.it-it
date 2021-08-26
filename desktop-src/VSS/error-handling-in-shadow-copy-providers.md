---
description: VSS consente l'esistenza di molte copie shadow contemporaneamente, ma consente solo la creazione di un set di copie shadow in corso tra la chiamata a IVssBackupComponents::StartSnapshotSet e il ritorno dalla chiamata a IVssBackupComponents::D oSnapshotSet.
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Gestione degli errori nei provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0963df4c9c81c2cd9f96e7c1828243f3910a1df34d5ef94a714f17c57b404b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032681"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Gestione degli errori nei provider di copie shadow

VSS consente l'esistenza di molte copie shadow contemporaneamente, ma consente solo la creazione di un set di copie shadow in corso tra la chiamata a [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e il ritorno dalla chiamata a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).

## <a name="no-partial-commit"></a>Nessun commit parziale

Se un provider non riesce a eseguire una copia shadow in qualsiasi volume o LUN nel set di copie shadow, la creazione dell'intero set di copie shadow non riesce. Questo si verifica per motivi strutturali. Questa progettazione semplifica i problemi di comportamento associati alla semantica degli errori parziali e mantiene un punto nel tempo coerente in tutte le copie shadow nel set.

## <a name="reporting-fault-conditions"></a>Segnalazione di condizioni di errore

Se si verifica un errore del provider o una condizione di errore, il provider deve registrare un errore nel registro eventi dell'applicazione. Ciò include, ma non solo, eventuali errori specifici del provider durante la creazione o l'importazione di un set di copie shadow o un errore di allocazione delle risorse per la copia shadow in scrittura dopo la creazione. Questa registrazione non deve essere attivata durante il periodo di tempo in cui i volumi nel set di copie shadow sono bloccati.

## <a name="valid-provider-return-values"></a>Valori restituiti del provider validi

Nella tabella seguente sono elencati i codici restituiti validi per i metodi del provider e i relativi significati.



| Valore                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>S \_ OK<br/>                                                                                                                     | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ OUTOFMEMORY<br/>                                                                                          | La memoria del provider è insufficiente o altre risorse di sistema.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | Uno dei valori del parametro non è valido.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ ACCESSO NEGATO<br/>                                                                                       | Un client senza privilegi ha tentato di chiamare nel provider.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>VSS \_ E \_ BAD \_ STATE<br/>                                                                                  | Nessun provider supporta l'operazione richiesta oppure l'operazione non può essere eseguita sull'oggetto perché l'oggetto non è nello stato corretto.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>OGGETTO \_ VSS E \_ \_ NON \_ TROVATO<br/>                                                            | Un parametro fa riferimento a un oggetto che non è stato trovato, ad esempio un ID copia shadow, un ID set di copie shadow o un volume.<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>SPAZIO DI ARCHIVIAZIONE INSUFFICIENTE DI VSS \_ E \_ \_<br/>                                                 | Il provider non può eseguire l'operazione perché lo spazio su disco non è sufficiente.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>VOLUME \_ VSS E \_ \_ NON \_ SUPPORTATO<br/>                                                | Nessun provider in questo computer supporta l'operazione richiesta nel volume.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>VOLUME VSS \_ E NON SUPPORTATO DAL \_ \_ \_ \_ \_ PROVIDER<br/>          | Il provider non supporta il volume.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>VSS \_ E NUMERO MASSIMO DI SNAPSHOT \_ \_ \_ \_ \_ RAGGIUNTO<br/> | Il provider ha raggiunto il numero massimo di copie shadow che può supportare.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>VETO DEL PROVIDER VSS \_ E \_ \_<br/>                                                                      | Il provider ha rilevato un errore di run-time interno che non esegue il mapping a un altro valore restituito. Il provider deve anche scrivere un evento nel registro eventi dell'applicazione fornendo all'utente informazioni su come risolvere il problema.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E NON PUÒ RIPRISTINARE \_ \_ \_ DISKID<br/>                                                | Impossibile impostare la firma MBR o l'ID GPT per uno o più dischi sul valore richiesto. Per altre informazioni, controllare il registro eventi dell'applicazione.<br/>                                                                                            |



 

Il provider non deve tentare di restituire altri codici di errore.

Se il provider restituisce un codice di errore non previsto (ad esempio **S \_ FALSE,** **E \_ FAIL,** **E \_ UNEXPECTED** o **E \_ ABORT),** VSS scrive un evento nel registro eventi indicando il provider e il metodo non riuscito e converte l'errore in **VSS E UNEXPECTED PROVIDER \_ \_ \_ \_ ERROR** prima di tornare al richiedente. Questa operazione non viene eseguita per i restituiti [**da IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) o [**IVssProviderNotifications::OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 





---
description: Un gestore di risorse viene integrato in una transazione quando inizia a partecipare alla transazione specifica.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Integrazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52820af2a7b280bc4740d0309fb627725e648685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233712"
---
# <a name="enlistments"></a>Integrazioni

Un gestore di risorse viene integrato in una transazione quando inizia a partecipare alla transazione specifica. L'integrazione definisce le notifiche accettate dal gestore di risorse. Un gestore di risorse crea un oggetto di integrazione quando si integra in una transazione. Questo oggetto segnala a KTM che Resource Manager (RM) richiede notifiche sulla transazione specificata.

RM fornisce una struttura [**di \_ maschera di notifica**](notification-mask.md) che specifica le notifiche richieste.

## <a name="enlistment-functions"></a>Funzioni di integrazione

Le funzioni seguenti vengono usate con gli elenchi.



| Funzione                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica che un gestore di risorse (RM) ha completato il commit di una transazione richiesta da Transaction Manager (TM).                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea un'integrazione, ne imposta lo stato iniziale e apre un handle per l'elenco con l'accesso specificato.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una struttura opaca dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di gestione risorse (RM) chiamando la funzione [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . In seguito a un errore, RM può utilizzare la funzione [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Apre un oggetto di integrazione esistente e restituisce un handle per l'integrazione.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Richiede che l'integrazione specificata venga convertita in un elenco di sola lettura. Un elenco di sola lettura non può partecipare al risultato della transazione e non viene registrato in modo durevole per il ripristino.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Esegue il rollback della transazione specificata associata a un'integrazione. Questa funzione non può essere chiamata per l'integrazione di sola lettura.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Imposta una struttura opaca definita dall'utente dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di gestione risorse (RM) chiamando [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). In seguito a un errore, il gestore di risorse può utilizzare [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica che Gestione risorse (RM) sta rifiutando una richiesta a fase singola. Quando una gestione transazioni riceve questa chiamata, avvia un commit a due fasi e invia una richiesta di preparazione a tutti i RMs integrati.                                                                                                                                                                                       |



 

 

 




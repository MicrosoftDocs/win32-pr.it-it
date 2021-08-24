---
description: Un gestore di risorse si integra in una transazione quando inizia la partecipazione a tale transazione specifica.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Integrazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19fea9c19da9bb16f81bd417e22c943876997ac224e3823020e5660218dfa5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146584"
---
# <a name="enlistments"></a>Integrazioni

Un gestore di risorse si integra in una transazione quando inizia la partecipazione a tale transazione specifica. L'integrazione definisce le notifiche accettate dal gestore di risorse. Un gestore di risorse crea un oggetto di integrazione quando si integra in una transazione. Questo oggetto segnala a KTM che il gestore di risorse (RM) richiede notifiche sulla transazione specificata.

L'RM fornisce [**una struttura NOTIFICATION \_ MASK**](notification-mask.md) che illustra in dettaglio le notifiche richieste.

## <a name="enlistment-functions"></a>Funzioni di integrazione

Le funzioni seguenti vengono usate con le integrazioni.



| Funzione                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica che un gestore di risorse ha completato il commit di una transazione richiesta dalla gestione transazioni.                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea un'integrazione, ne imposta lo stato iniziale e apre un handle per l'integrazione con l'accesso specificato.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una struttura opaca dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di un gestore di risorse chiamando la [**funzione SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Dopo un errore, l'RM può usare [**la funzione GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Apre un oggetto di integrazione esistente e restituisce un handle per l'integrazione.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Richiede che l'integrazione specificata sia convertita in un'integrazione di sola lettura. Un'integrazione di sola lettura non può partecipare al risultato della transazione e non viene registrata in modo durevole per il recupero.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Esegue il rollback della transazione specificata associata a un'integrazione. Questa funzione non può essere chiamata per le integrazioni di sola lettura.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Imposta una struttura opaca definita dall'utente dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di un gestore di risorse chiamando [**SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Dopo un errore, l'RM può [**usare GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica che il gestore di risorse rifiuta una richiesta a fase singola. Quando una gestione transazioni riceve questa chiamata, avvia un commit in due fasi e invia una richiesta di preparazione a tutte le macchine virtuali integrate.                                                                                                                                                                                       |



 

 

 




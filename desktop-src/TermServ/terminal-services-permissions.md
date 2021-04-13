---
title: Autorizzazioni Servizi Desktop remoto
description: È possibile utilizzare le autorizzazioni fornite per Servizi Desktop remoto per controllare la modalità di accesso di utenti e gruppi al server.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1358a4360889bc013beefcee4e029f3572c9c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399142"
---
# <a name="remote-desktop-services-permissions"></a>Autorizzazioni Servizi Desktop remoto

È possibile utilizzare le autorizzazioni fornite per Servizi Desktop remoto per controllare la modalità di accesso di utenti e gruppi al server. Per una descrizione dei tipi di autorizzazione predefiniti e per informazioni più dettagliate sulle autorizzazioni Servizi Desktop remoto in generale, vedere la documentazione fornita con lo strumento di amministrazione Configurazione Servizi Desktop remoto. Per informazioni sulla configurazione di queste autorizzazioni per Windows Server 2008, vedere [configurare le autorizzazioni per le connessioni Servizi Desktop remoto](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11)).

Di seguito è riportato un elenco delle autorizzazioni che è possibile impostare e delle attività consentite dalle autorizzazioni.



| Valore                        | Significato                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informazioni sulle query<br/> | Eseguire query su sessioni e server per ottenere informazioni.<br/>                                                                                                                |
| Informazioni sui set<br/>   | Configurare le proprietà di connessione.<br/>                                                                                                                           |
| Controllo remoto<br/>    | Visualizza o controlla attivamente la sessione di un altro utente.<br/>                                                                                                           |
| Accesso<br/>             | Accedere a una sessione nel server.<br/>                                                                                                                         |
| Disconnessione<br/>            | Disconnettere un utente da una sessione. Tenere presente che la disconnessione di un utente senza avviso può causare la perdita di dati nel client.<br/>                                  |
| Message<br/>           | Invia un messaggio alle sessioni di un altro utente.<br/>                                                                                                                 |
| Connessione<br/>           | Connettersi a un'altra sessione.<br/>                                                                                                                                |
| Disconnetti<br/>        | Disconnettere una sessione.<br/>                                                                                                                                      |
| Canali virtuali<br/>  | Usare i canali virtuali. Tenere presente che la disattivazione di canali virtuali Disabilita alcune Servizi Desktop remoto funzionalità come gli appunti e il reindirizzamento della stampante.<br/> |
| Reset<br/>             | Terminare una sessione. Tenere presente che la chiusura di una sessione senza avviso può causare la perdita di dati nel client.<br/>                                                    |



 

L'autorizzazione di accesso è necessaria per l'accesso di un utente a una nuova sessione di Servizi Desktop remoto. Tutte le altre Servizi Desktop remoto autorizzazioni si applicano al controllo Servizi Desktop remoto sessione di un altro utente.

È possibile concedere o impostare autorizzazioni Servizi Desktop remoto per singoli utenti o gruppi. Gli utenti possono anche ereditare le autorizzazioni come risultato di un membro del gruppo. Il rifiuto di un'autorizzazione, tuttavia, esegue l'override di un'autorizzazione ereditata. Ai membri del gruppo Desktop remoto Users (RDU), ad esempio, viene concessa l'autorizzazione per la query per impostazione predefinita. Se un amministratore imposta l'autorizzazione per la query su "Nega" per tale utente, l'utente non sarà in grado di eseguire query su un'altra sessione dell'utente. Dopo che un utente ha eseguito l'accesso a una sessione, all'utente vengono concesse tutte le altre Servizi Desktop remoto autorizzazioni per la propria sessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni di gestione Servizi Desktop remoto](terminal-services-management-applications.md)
</dt> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> </dl>

 


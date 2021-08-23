---
title: Servizi Desktop remoto autorizzazioni
description: È possibile usare le autorizzazioni fornite per Servizi Desktop remoto controllare il modo in cui utenti e gruppi accedono al server.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 668bf4902ffb133c403e5ea2f74bbc165cf99bca500c95eed5d5dac3cb48a710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999891"
---
# <a name="remote-desktop-services-permissions"></a>Servizi Desktop remoto autorizzazioni

È possibile usare le autorizzazioni fornite per Servizi Desktop remoto controllare il modo in cui utenti e gruppi accedono al server. Per una descrizione dei tipi di autorizzazione predefiniti e per informazioni più dettagliate sulle autorizzazioni Servizi Desktop remoto in generale, vedere la documentazione che accompagna lo strumento di amministrazione Servizi Desktop remoto Configuration. Per informazioni sulla configurazione di queste autorizzazioni per Windows Server 2008, vedere Configurare le autorizzazioni per [Servizi Desktop remoto connessioni .](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11))

Di seguito è riportato un elenco delle autorizzazioni che è possibile impostare e delle attività consentite.



| Valore                        | Significato                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informazioni query<br/> | Per informazioni, eseguire query su sessioni e server.<br/>                                                                                                                |
| Impostare le informazioni<br/>   | Configurare le proprietà di connessione.<br/>                                                                                                                           |
| Controllo remoto<br/>    | Visualizzare o controllare attivamente la sessione di un altro utente.<br/>                                                                                                           |
| Accesso<br/>             | Accedere a una sessione nel server.<br/>                                                                                                                         |
| Disconnessione<br/>            | Disconnettere un utente da una sessione. Tenere presente che la disconnessione di un utente senza avviso può comportare la perdita di dati nel client.<br/>                                  |
| Message<br/>           | Inviare un messaggio alle sessioni di un altro utente.<br/>                                                                                                                 |
| Connettere<br/>           | Connessione a un'altra sessione.<br/>                                                                                                                                |
| Disconnetti<br/>        | Disconnettere una sessione.<br/>                                                                                                                                      |
| Canali virtuali<br/>  | Usare canali virtuali. Tenere presente che la disattivazione dei canali virtuali disabilita alcune Servizi Desktop remoto, ad esempio gli Appunti e il reindirizzamento della stampante.<br/> |
| Reset<br/>             | Terminare una sessione. Tenere presente che la chiusura di una sessione senza avviso può comportare la perdita di dati nel client.<br/>                                                    |



 

L'autorizzazione di accesso è necessaria per l'accesso di un utente a una nuova Servizi Desktop remoto sessione. Tutte le Servizi Desktop remoto autorizzazioni si applicano al controllo della sessione Servizi Desktop remoto un altro utente.

Servizi Desktop remoto possono essere concesse o impostate autorizzazioni per singoli utenti o gruppi. Gli utenti possono anche ereditare le autorizzazioni in seguito all'appartenenza a un gruppo. La negazione di un'autorizzazione, tuttavia, sostituisce un'autorizzazione ereditata. Ad esempio, ai membri del gruppo Desktop remoto utenti (RDU) viene concessa l'autorizzazione Query per impostazione predefinita. Se un amministratore imposta l'autorizzazione query su "Nega" per tale utente, l'utente non sarà in grado di eseguire query sulla sessione di un altro utente. Dopo l'accesso di un utente a una sessione, all'utente vengono concesse tutte le altre Servizi Desktop remoto per la sessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi Desktop remoto applicazioni di gestione](terminal-services-management-applications.md)
</dt> <dt>

[**Account \_ TS Win32**](win32-tsaccount.md)
</dt> </dl>

 


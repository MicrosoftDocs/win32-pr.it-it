---
title: Utente interattivo
description: L'utente interattivo è l'utente attualmente connesso al computer in cui è in esecuzione il server COM.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339319"
---
# <a name="interactive-user"></a>Utente interattivo

L' *utente interattivo* è l'utente attualmente connesso al computer in cui è in esecuzione il server com. Se l'identità è impostata come utente interattivo, tutti i client utilizzeranno la stessa istanza del server se il server ne registrerà il class factory come multiutilizzo. Se nessun utente è connesso, il server non verrà eseguito. Se il server dispone di un'interfaccia utente grafica (GUI) che il client deve visualizzare, è necessario usare l'utente interattivo per l'identità del server. Tuttavia, la scelta di questa identità comporta alcuni rischi per la sicurezza perché il server viene eseguito con l'identità dell'utente che ha effettuato l'accesso senza la conoscenza o il consenso dell'utente connesso. Inoltre, un'applicazione di servizio non è in grado di visualizzare un'interfaccia utente. Per ulteriori informazioni, vedere [servizi interattivi](/windows/desktop/Services/interactive-services).

Se un server COM è configurato per l'esecuzione come utente interattivo, in un ambiente di Servizi terminal, il server verrà avviato nella sessione interattiva corrispondente all'identità utente del client. Tuttavia, l'applicazione client può utilizzare il moniker della sessione per fare riferimento a un oggetto fornito dal server in una sessione che non corrisponde all'identità del client. Quando si utilizza questo, l'applicazione client può specificare qualsiasi sessione, nel qual caso il server verrà eseguito con l'utente proprietario della sessione e non con l'utente di avvio. Le autorizzazioni di accesso predefinite in questo scenario non consentono all'utente di avviare di chiamare i metodi sul server. Tuttavia, vengono mantenuti i rischi di sicurezza seguenti:

-   Se il server COM espone interfacce che non sono controllate da COM, ad esempio porte TCP, named pipe, porte LPC, sezioni Shared Memory e così via, possono essere usate dall'utente che ha avviato l'avvio per influenzare il server. Gli oggetti COM configurati per l'esecuzione come utente interattivo dovrebbero ridurre al massimo la superficie di attacco.
-   Gli oggetti COM sono gratuiti per impostare le proprie autorizzazioni di accesso. Se l'oggetto imposta le autorizzazioni di accesso, nella registrazione AppID o chiamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), per consentire all'utente di avviare l'accesso, l'utente può avviare il server per l'esecuzione con un altro utente, quindi accedere all'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Identità applicazione](application-identity.md)
</dt> <dt>

[Avvio dell'utente](launching-user.md)
</dt> <dt>

[Identità del servizio](service-identity.md)
</dt> <dt>

[Utente specificato](specified-user.md)
</dt> </dl>

 

 
---
title: Utente interattivo
description: L'utente interattivo è l'utente attualmente connesso al computer in cui è in esecuzione il server COM.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d842a468634da0eba31b04317b66185b298fc5a2e44d3567f796dac52dbdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992731"
---
# <a name="interactive-user"></a>Utente interattivo

*L'utente* interattivo è l'utente attualmente connesso al computer in cui è in esecuzione il server COM. Se l'identità è impostata come utente interattivo, tutti i client usano la stessa istanza del server se il server registra il class factory come multi-uso. Se nessun utente è connesso, il server non verrà eseguito. Se il server ha un'interfaccia utente grafica (GUI) che il client deve visualizzare, è consigliabile usare l'utente interattivo per l'identità del server. Tuttavia, la scelta di questa identità comporta alcuni rischi per la sicurezza perché il server viene eseguito con l'identità dell'utente connesso senza la conoscenza o il consenso dell'utente connesso. Inoltre, un'applicazione di servizio non può visualizzare un'interfaccia utente. Per altre informazioni, vedere [Servizi interattivi](/windows/desktop/Services/interactive-services).

Se un server COM è configurato per l'esecuzione come utente interattivo, in un ambiente di Servizi terminal il server verrà avviato nella sessione interattiva corrispondente all'identità utente del client. Tuttavia, l'applicazione client può usare il moniker di sessione per fare riferimento a un oggetto fornito dal server in una sessione che non corrisponde all'identità del client. Quando viene usato, l'applicazione client può specificare qualsiasi sessione, nel qual caso il server verrà eseguito come utente proprietario della sessione, non come utente di avvio. Le autorizzazioni di accesso predefinite in questo scenario non consentono all'utente che avvia di chiamare metodi sul server. Rimangono tuttavia i rischi per la sicurezza seguenti:

-   Se il server COM espone interfacce non controllate da COM, ad esempio porte TCP, named pipe, porte LPC, sezioni di memoria condivisa e così via, queste potrebbero essere usate dall'utente che avvia per influenzare il server. Gli oggetti COM configurati per l'esecuzione come utente interattivo devono ridurre il più possibile questa superficie di attacco.
-   Gli oggetti COM possono impostare le proprie autorizzazioni di accesso. Se l'oggetto imposta le autorizzazioni di accesso, nella registrazione AppID o chiamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), per consentire all'utente che avvia l'accesso, l'utente sarà in grado di avviare il server per l'esecuzione come altro utente e quindi accedere all'oggetto.

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

 

 
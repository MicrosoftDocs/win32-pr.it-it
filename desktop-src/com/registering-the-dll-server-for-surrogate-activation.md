---
title: Registrazione del server DLL per l'attivazione surrogata
description: Registrazione del server DLL per l'attivazione surrogata
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730466"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>Registrazione del server DLL per l'attivazione surrogata

Un server DLL verrà caricato in un processo surrogato nelle condizioni seguenti:

-   È necessario specificare un valore AppID nella chiave CLSID nel registro di sistema e una chiave [AppID](appid-key.md) corrispondente.
-   In una chiamata di attivazione, viene impostato il bit del [**\_ \_ server locale CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e la chiave CLSID non specifica [LocalServer32](localserver32.md), [LocalServer](localserver.md)o [LocalService](localservice.md). Se sono impostati altri bit **CLSCTX** , viene seguito l' [**algoritmo di elaborazione**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)per i flag di esecuzione in-process, locali o remoti.
-   La chiave CLSID contiene la sottochiave [InprocServer32](inprocserver32.md) .
-   La DLL proxy/stub specificata nella chiave **InprocServer32** esiste.
-   Il valore [DllSurrogate](dllsurrogate.md) esiste sotto la chiave **AppID** .

Se è presente un **LocalServer**, **LocalServer32** o **LocalService**, che indica l'esistenza di un file exe, il server o il servizio exe viene sempre avviato in preferenza al caricamento di un server DLL in un processo surrogato.

È necessario specificare il valore denominato **DllSurrogate** per l'attivazione surrogata. L'attivazione si riferisce alle chiamate a una delle funzioni di attivazione seguenti:

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

Per avviare un'istanza del surrogato fornito dal sistema, impostare il valore di **DllSurrogate** su una stringa vuota o su **null**. Per specificare l'avvio di un surrogato personalizzato, impostare il valore sul percorso del surrogato.

Se vengono specificati sia [RemoteServerName](remoteservername.md) che **DllSurrogate** per lo stesso AppID, il valore **RemoteServerName** viene ignorato e il valore **DllSurrogate** causa un'attivazione nel computer locale. Per l'attivazione surrogata remota, specificare **RemoteServerName** ma non **DllSurrogate** nel client e specificare **DllSurrogate** nel server.

Un server DLL progettato per essere sempre eseguito da solo nel proprio processo surrogato è migliore per la configurazione con un AppID uguale al relativo CLSID. In **AppID** è sufficiente specificare un valore denominato **DllSurrogate** con un valore di stringa vuoto.

È consigliabile configurare un server DLL progettato per essere eseguito da solo nel proprio processo surrogato e per servire più client in una rete con un valore [RunAs](runas.md) specificato nella chiave del registro di sistema **AppID** . Se **RunAs** specifica "utente interattivo" o un'identità utente specifica dipende dall'interfaccia utente, dalla sicurezza e da altri requisiti del server. Quando si specifica un valore **RunAs** , viene caricata solo un'istanza del server per il servizio di tutti i client, indipendentemente dall'identità del client. D'altra parte, non configurare il server con **RunAs** se si intende disporre di un'istanza del server DLL in esecuzione in surrogato per servire ogni identità client remota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti del server DLL](dll-server-requirements.md)
</dt> <dt>

[Condivisione surrogati](surrogate-sharing.md)
</dt> </dl>

 

 
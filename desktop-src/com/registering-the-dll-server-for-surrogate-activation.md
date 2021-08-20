---
title: Registrazione del server DLL per l'attivazione surrogata
description: Registrazione del server DLL per l'attivazione surrogata
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0e32c3c6e42705b8cfa338c280f5edf502eb22df84764d2f774f496dc70dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104821"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>Registrazione del server DLL per l'attivazione surrogata

Un server DLL verrà caricato in un processo surrogato nelle condizioni seguenti:

-   Deve essere presente un valore AppID specificato sotto la chiave CLSID nel Registro di sistema e una chiave [AppID](appid-key.md) corrispondente.
-   In una chiamata di attivazione viene impostato il bit [**CLSCTX \_ LOCAL \_ SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e la chiave CLSID non specifica [LocalServer32,](localserver32.md) [LocalServer](localserver.md)o [LocalService.](localservice.md) Se vengono impostati altri bit **CLSCTX,** viene seguito l'algoritmo di elaborazione per i flag di esecuzione in-process, locali o remoti. [](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
-   La chiave CLSID contiene la [sottochiave InprocServer32.](inprocserver32.md)
-   La DLL proxy/stub specificata nella chiave **InprocServer32** esiste.
-   Il [valore DllSurrogate](dllsurrogate.md) esiste sotto la **chiave AppID.**

Se è presente un **localServer**, **LocalServer32** o **LocalService**, che indica l'esistenza di un file EXE, il server o il servizio EXE verrà sempre avviato in preferenza per il caricamento di un server DLL in un processo surrogato.

Per eseguire l'attivazione surrogata, è necessario specificare il valore denominato **DllSurrogate.** L'attivazione si riferisce alle chiamate a una delle funzioni di attivazione seguenti:

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

Per avviare un'istanza del surrogato fornito dal sistema, impostare il valore di **DllSurrogate** su una stringa vuota o su **NULL.** Per specificare l'avvio di un surrogato personalizzato, impostare il valore sul percorso del surrogato.

Se vengono [specificati sia RemoteServerName](remoteservername.md) che **DllSurrogate** per lo stesso AppID, il valore **RemoteServerName** viene ignorato e il **valore DllSurrogate** causa un'attivazione nel computer locale. Per l'attivazione surrogata remota, specificare **RemoteServerName** ma non **DllSurrogate** nel client e **dllSurrogate** nel server.

Un server DLL progettato per essere sempre eseguito da solo nel proprio processo surrogato è configurato in modo ottimale con un AppID uguale al relativo CLSID. In **AppID** specificare semplicemente un valore denominato **DllSurrogate** con un valore stringa vuoto.

È meglio configurare un server DLL progettato per l'esecuzione autonoma nel proprio processo surrogato e per la gestione di più client in una rete con un valore [RunAs](runas.md) specificato nella chiave del Registro di sistema **AppID.** Il fatto **che RunAs** specifichi "Interactive User" o un'identità utente specifica dipende dall'interfaccia utente, dalla sicurezza e da altri requisiti del server. Quando viene specificato un valore **RunAs,** viene caricata solo un'istanza del server per la gestione di tutti i client, indipendentemente dall'identità del client. D'altra parte, non configurare il server con **RunAs** se si intende avere un'istanza del server DLL in esecuzione in surrogato per la gestione di ogni identità client remota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti del server DLL](dll-server-requirements.md)
</dt> <dt>

[Condivisione di surrogati](surrogate-sharing.md)
</dt> </dl>

 

 
---
title: In-Context delle funzioni Hook
description: Per motivi di prestazioni, gli sviluppatori client registrano funzioni hook nel contesto.
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1333cf7718ff954217170e89dce2af70cc081fcca18929282f6db4a188125b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565589"
---
# <a name="in-context-hook-function-precautions"></a>In-Context delle funzioni Hook

Per motivi di prestazioni, gli sviluppatori client registrano funzioni hook nel contesto. Tuttavia, poiché queste funzioni hook vengono mappate nello spazio degli indirizzi del server, gli sviluppatori di client e server devono adottare precauzioni per garantire che l'elaborazione degli eventi funzioni senza problemi.

## <a name="precautions-for-client-developers"></a>Precauzioni per gli sviluppatori client

Gli sviluppatori client devono essere a conoscenza dei problemi seguenti:

-   Le funzioni hook nel contesto non devono usare molto tempo del processore, perché la funzione hook deve restituire prima che l'applicazione server continui.
-   Dopo l'attivazione di un evento, è possibile che la finestra associata a un evento non esista più quando viene chiamata la funzione hook. I client devono verificare che la finestra associata a un evento esista ancora prima di eseguire qualsiasi altra azione correlata all'evento. Per assicurarsi che una finestra esista ancora, i client usano la funzione Microsoft Win32 [**IsWindow.**](/windows/desktop/api/winuser/nf-winuser-iswindow)
-   Se la DLL in cui è definita la funzione hook è collegata a un'altra DLL, gli sviluppatori client devono assicurarsi che il sistema carichi l'altra DLL. Se si esegue il collegamento in modo implicito (usando file def e importazioni), la DLL aggiuntiva deve essere nella directory Windows o in una delle directory di sistema, ad esempio Windows \\ System, Windows \\ System32 o Windows \\ SysWOW64. Se si collega in modo esplicito (usando [**LoadLibrary),**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)il percorso completo della directory in cui si trova la DLL aggiuntiva deve essere specificato nella chiamata a **LoadLibrary**.
-   Le funzioni hook nel contesto possono causare un overflow dello stack quando la DLL che contiene la funzione hook viene caricata in un'applicazione a 16 bit. Questo problema si verifica perché le applicazioni a 16 bit usano dimensioni dello stack fisse non sufficientemente grandi da contenere la catena di chiamate di funzioni di sistema che comportano una chiamata alla funzione hook.

## <a name="precautions-for-server-developers"></a>Precauzioni per gli sviluppatori di server

Gli sviluppatori di server devono essere consapevoli del fatto che le applicazioni client potrebbero registrare funzioni hook nel contesto. Quando un server chiama [**NotifyWinEvent,**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)deve essere preparato per gestire [**WM \_ GETOBJECT**](wm-getobject.md) e altri [**metodi IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

## <a name="invalid-interface-pointers"></a>Puntatori a interfaccia non validi

Quando un client chiama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) all'interno di una funzione hook nel contesto, il puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) restituito punta direttamente al codice nello spazio degli indirizzi del server. Se il client chiama una proprietà dell'interfaccia usando questo puntatore, la libreria Component Object Model (COM) non è coinvolta nel marshalling (creazione di pacchetti e invio di parametri di interfaccia attraverso i limiti del processo) o annullamento del marshalling (decompressione dei parametri inviati oltre i limiti del processo) e non rileva se un oggetto viene eliminato.

Se il client chiama una proprietà dell'interfaccia a un oggetto eliminato, il puntatore a interfaccia non valido causa un errore di protezione generale nello spazio indirizzi del server, a meno che il server non rilevi questa situazione.

Per proteggersi da puntatori a interfaccia non validi, i server [creano oggetti proxy che](creating-proxy-objects.md) esercitino il wrapping degli oggetti accessibili e monitorino l'intervallo di vita degli oggetti accessibili. Ad esempio, quando un client chiama una proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per ottenere informazioni su un oggetto, il proxy verifica se l'oggetto accessibile è ancora disponibile e, in tal caso, inoltra la richiesta del client all'oggetto accessibile. Se l'oggetto accessibile viene eliminato, il proxy restituisce un errore al client.

 

 
---
title: Precauzioni della funzione hook In-Context
description: Per motivi di prestazioni, gli sviluppatori client registrano funzioni hook nel contesto.
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e319037cb1295725548b3361bf076b4b1f760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300125"
---
# <a name="in-context-hook-function-precautions"></a>Precauzioni della funzione hook In-Context

Per motivi di prestazioni, gli sviluppatori client registrano funzioni hook nel contesto. Tuttavia, poiché queste funzioni hook sono mappate nello spazio degli indirizzi del server, gli sviluppatori di client e server devono adottare le precauzioni necessarie per garantire che l'elaborazione degli eventi venga eseguita senza problemi.

## <a name="precautions-for-client-developers"></a>Precauzioni per gli sviluppatori client

Gli sviluppatori client devono essere a conoscenza dei seguenti problemi:

-   Le funzioni hook nel contesto non devono utilizzare molto tempo del processore, perché la funzione hook deve restituire prima che l'applicazione server continui.
-   Dopo l'attivazione di un evento, è possibile che la finestra associata a un evento non esista più nel momento in cui viene chiamata la funzione hook. I client devono verificare che la finestra associata a un evento esista ancora prima di intraprendere qualsiasi altra azione correlata all'evento. Per assicurarsi che esista ancora una finestra, i client utilizzano la funzione [**finestra**](/windows/desktop/api/winuser/nf-winuser-iswindow) di Microsoft Win32.
-   Se la DLL in cui è definita la funzione hook è collegata a un'altra DLL, gli sviluppatori client devono assicurarsi che il sistema carichi l'altra DLL. Se si collega in modo implicito (usando i file def e le importazioni), la DLL aggiuntiva deve trovarsi nella directory di Windows o in una delle directory di sistema, ad esempio Windows \\ System, Windows \\ System32 o Windows \\ SysWow64. Se si collega in modo esplicito (usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)), il percorso completo della directory in cui risiede la DLL aggiuntiva deve essere specificato nella chiamata a **LoadLibrary**.
-   Le funzioni hook nel contesto possono causare un overflow dello stack quando la DLL che contiene la funzione hook viene caricata in un'applicazione a 16 bit. Questo problema si verifica perché le applicazioni a 16 bit utilizzano una dimensione dello stack fissa non sufficientemente grande da contenere la catena di chiamate di funzione di sistema che generano una chiamata alla funzione hook.

## <a name="precautions-for-server-developers"></a>Precauzioni per gli sviluppatori di server

Gli sviluppatori di server devono tenere presente che le applicazioni client possono registrare funzioni hook nel contesto. Quando un server chiama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), deve essere preparato per gestire [**WM \_ GetObject**](wm-getobject.md) e altri metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="invalid-interface-pointers"></a>Puntatori a interfaccia non validi

Quando un client chiama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) all'interno di una funzione hook nel contesto, il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) restituito punta direttamente al codice nello spazio degli indirizzi del server. Se il client chiama una proprietà di interfaccia usando questo puntatore, la libreria Component Object Model (COM) non è associata al marshalling (creazione di pacchetti e invio di parametri di interfaccia tra i limiti del processo) o all'annullamento del marshalling (annullamento del packaging dei parametri inviati attraverso i limiti del processo) e non rileva se un oggetto viene eliminato definitivamente.

Se il client chiama una proprietà di interfaccia a un oggetto che viene eliminato definitivamente, il puntatore a interfaccia non valido causa un errore di protezione generale nello spazio degli indirizzi del server, a meno che il server non rilevi questa situazione.

Per proteggersi da puntatori di interfaccia non validi, i server [creano oggetti proxy](creating-proxy-objects.md) che esegue il wrapping degli oggetti accessibili e monitora la durata degli oggetti accessibili. Ad esempio, quando un client chiama una proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per ottenere informazioni su un oggetto, il proxy controlla se l'oggetto accessibile è ancora disponibile e, in caso affermativo, esegue il inoltro della richiesta del client all'oggetto accessibile. Se l'oggetto accessibile viene eliminato definitivamente, il proxy restituisce un errore al client.

 

 
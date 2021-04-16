---
title: Ricerca e caricamento delle risorse
description: In questo argomento viene illustrato come caricare una risorsa in memoria.
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca9590927cad28772a6b4a5b761d74c9ebf101a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472827"
---
# <a name="finding-and-loading-resources"></a>Ricerca e caricamento delle risorse

Prima di usare una risorsa, un'applicazione deve caricarla in memoria. Le funzioni [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) e [**FindResourceEx**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa) trovano una risorsa in un modulo e restituiscono un handle ai dati della risorsa binaria. **FindResource** individua una risorsa in base al tipo e al nome. **FindResourceEx** individua la risorsa in base al tipo, al nome e alla lingua. Le informazioni su **FindResource** in questo argomento si applicano anche a **FindResourceEx**.

La funzione [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) usa l'handle di risorsa restituito da [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) per caricare la risorsa in memoria. Dopo che un'applicazione ha caricato una risorsa usando **LoadResource**, il sistema Scarica la memoria associata solo quando tutti i riferimenti al relativo modulo vengono liberati tramite [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Le applicazioni che devono accedere ripetutamente alle stesse risorse o a molte risorse all'interno di un particolare modulo possono comportare sanzioni delle prestazioni a causa del mapping della memoria che si verifica nelle chiamate ripetute [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e **FreeLibrary** . Le applicazioni devono archiviare un singolo handle del modulo fino a quando le risorse non sono più necessarie, quindi chiamare **FreeLibrary**. Dopo che un modulo è stato scaricato dalla memoria, gli handle di risorsa diventano non validi.

Un'applicazione può usare [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) e [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) per trovare e caricare qualsiasi tipo di risorsa, ma queste funzioni devono essere usate solo in una delle situazioni seguenti:

-   Quando l'applicazione non è in grado di accedere alla risorsa utilizzando una funzione specifica della risorsa esistente.
-   Quando l'applicazione deve accedere alla risorsa come dati binari per le successive chiamate di funzione.

Quando possibile, un'applicazione deve invece usare una delle funzioni specifiche delle risorse seguenti per trovare e caricare le risorse in un'unica chiamata:



| Funzione                                     | Azione                                   | Per rimuovere la risorsa                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | Carica e formatta una voce della tabella di messaggio. | Non è richiesta alcuna azione.                                                                                                |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | Carica una tabella dei tasti di scelta rapida.              | [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | Carica una risorsa bitmap.                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | Carica una risorsa di cursore.                 | [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | Carica una risorsa icona.                  | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | Carica un'icona, un cursore o una bitmap.        | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon), [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor), [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | Carica una risorsa di menu.                   | [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | Carica una voce della tabella di stringhe.              | Non è richiesta alcuna azione.                                                                                                |



 

Prendere nota delle funzioni di rilascio nella tabella precedente. Prima di terminare, un'applicazione deve rilasciare la memoria occupata da tabelle di tasti di scelta rapida, bitmap, cursori, icone e menu utilizzando le funzioni appropriate.

La memoria associata alle risorse caricate tramite [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) e [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) verrà rilasciata una volta che il modulo è stato scaricato da una chiamata a [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Tutte le risorse che rimangono scaricate alla chiusura dell'applicazione verranno rilasciate automaticamente dal sistema.

 

 
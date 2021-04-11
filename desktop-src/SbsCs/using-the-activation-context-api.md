---
description: Le applicazioni possono gestire un contesto di attivazione chiamando direttamente le funzioni del contesto di attivazione.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Uso dell'API del contesto di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128810"
---
# <a name="using-the-activation-context-api"></a>Uso dell'API del contesto di attivazione

Le applicazioni possono gestire un [contesto di attivazione](activation-contexts.md) chiamando direttamente le funzioni del contesto di attivazione. I contesti di attivazione sono strutture dei dati in memoria. Il sistema può utilizzare le informazioni nel contesto di attivazione per reindirizzare un'applicazione in modo da caricare una particolare versione della DLL, un'istanza dell'oggetto COM o una versione della finestra personalizzata. Per altre informazioni, vedere [riferimento al contesto di attivazione](activation-context-reference.md).

Il Application Programming Interface (API) può essere usato per gestire il contesto di attivazione e creare oggetti con nome di versione con [manifesti](manifests.md). Nei due scenari seguenti viene illustrato il modo in cui un'applicazione può gestire un contesto di attivazione chiamando direttamente le funzioni del contesto di attivazione. Nella maggior parte dei casi, tuttavia, il contesto di attivazione è gestito dal sistema. Gli sviluppatori di applicazioni e i provider di assembly non devono in genere effettuare chiamate allo stack per gestire il contesto di attivazione.

-   Processi e applicazioni che implementano livelli di riferimento indiretto o di invio.

    Ad esempio, un utente che gestisce i contesti di attivazione nel ciclo di eventi. Ogni volta che si accede alla finestra, ad esempio spostando il puntatore del mouse sulla finestra, viene chiamato [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) , che attiva il contesto di attivazione corrente per la risorsa, come illustrato nel frammento di codice seguente.

    <dl> GESTISCi hActCtx;  
    CreateWindow ();  
    ...  
    GetCurrentActCtx (&ActCtx);  
    ...  
    ReleaseActCtx (&ActCtx);  
    </dl>

    Nel frammento di codice seguente la funzione API attiva i contesti di attivazione appropriati prima di chiamare [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). Quando viene chiamato **CallWindowProc** , questo contesto viene usato per passare un messaggio a Windows. Al termine di tutte le operazioni sulle risorse, la funzione disattiverà il contesto.

    <dl> \_UlpCookie PTR ULONG;  
    GESTISCi hActCtx;  
    if (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    CallWindowProc (...);  
    ...  
    DeactivateActCtx (0, ulpCookie);  
    }  
    </dl>

-   Livello di invio del delegato.

    Questo scenario si applica ai manager che gestiscono più entità con un livello API comune, ad esempio una gestione driver. Sebbene non sia ancora stato implementato, un esempio è costituito dal driver ODBC.

    In questo scenario, il livello intermedio diventa in grado di elaborare le associazioni di assembly. Per ottenere il driver di associazione specifico della versione, è necessario che i Publisher forniscano un manifesto e specifichino le dipendenze da componenti specifici del manifesto. L'applicazione di base non esegue un'associazione dinamica ai componenti; in fase di esecuzione, gestione driver gestisce le chiamate. Quando il driver ODBC viene chiamato in base alla stringa di connessione, carica il driver appropriato. Quindi crea il contesto di attivazione usando le informazioni contenute nel file manifesto dell'assembly.

    Senza il manifesto, l'azione predefinita per il driver prevede l'uso dello stesso contesto di quello specificato dall'applicazione, in questo esempio la versione 2 di MSVCRT. Poiché un manifesto esiste, viene stabilito un contesto di attivazione separato. Quando il driver ODBC viene eseguito, viene associato alla versione 1 dell'assembly MSVCRT.

    Ogni volta che Gestione driver chiama il livello di invio, ad esempio per ottenere il set di dati successivo, USA gli assembly appropriati in base al contesto di attivazione. Il frammento di codice seguente illustra questa operazione.

    <dl> GESTISCi hActCtx;  
    \_UlpCookie PTR ULONG;  
    ACTCTX ActCtxToCreate = {...};  
    hActCtx = CreateActCtx (&ActCtxToCreate);  
    ...;  
    if (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    ConnectDb(...);  
    DeactivateActCtx (0, ulpCookie);  
    }  
    ...  
    ReleaseActCtx(hActCtx);  
    </dl>

 

 

---
description: Le applicazioni possono gestire un contesto di attivazione chiamando direttamente le funzioni del contesto di attivazione.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Uso dell'API del contesto di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c2f3d1c1a6b6202619b9e39df6ee4dc60b9134ebefa9cfe7dea4db9a344bd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073301"
---
# <a name="using-the-activation-context-api"></a>Uso dell'API del contesto di attivazione

Le applicazioni possono gestire un [contesto di attivazione](activation-contexts.md) chiamando direttamente le funzioni del contesto di attivazione. I contesti di attivazione sono strutture di dati in memoria. Il sistema può usare le informazioni nel contesto di attivazione per reindirizzare un'applicazione al caricamento di una determinata versione della DLL, di un'istanza di oggetto COM o di una versione di finestra personalizzata. Per altre informazioni, vedere Informazioni [di riferimento sul contesto di attivazione.](activation-context-reference.md)

L'API (Application Programming Interface) può essere usata per gestire il contesto di attivazione e creare oggetti con nome di versione con [manifesti](manifests.md). I due scenari seguenti illustrano come un'applicazione può gestire un contesto di attivazione chiamando direttamente le funzioni del contesto di attivazione. Nella maggior parte dei casi, tuttavia, il contesto di attivazione è gestito dal sistema. Gli sviluppatori di applicazioni e i provider di assembly in genere non devono effettuare chiamate nello stack per gestire il contesto di attivazione.

-   Processi e applicazioni che implementano livelli di riferimento indiretto o dispatch.

    Ad esempio, un utente che gestisce i contesti di attivazione nel ciclo di eventi. Ogni volta che si accede alla finestra, ad esempio spostando il mouse sulla finestra, viene chiamato [**ActivateActCtx,**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) che attiva il contesto di attivazione corrente per la risorsa, come illustrato nel frammento di codice seguente.

    <dl> HANDLE hActCtx;  
    CreateWindow();  
    ...  
    GetCurrentActCtx(&ActCtx);  
    ...  
    ReleaseActCtx(&ActCtx);  
    </dl>

    Nel frammento di codice seguente la funzione API attiva i contesti di attivazione appropriati prima di [**chiamare CallWindowProc.**](/windows/win32/api/winuser/nf-winuser-callwindowproca) Quando **viene chiamato CallWindowProc,** usa questo contesto per passare un messaggio Windows. Al termine di tutte le operazioni sulle risorse, la funzione disattiva il contesto.

    <dl> ULONG \_ PTR ulpCookie;  
    HANDLE hActCtx;  
    if(ActivateActCtx(hActCtx, &ulpCookie))  
    {  
    ...  
    CallWindowProc(...);  
    ...  
    DeactivateActCtx(0, ulpCookie);  
    }  
    </dl>

-   Livello di invio del delegato.

    Questo scenario si applica ai responsabili che gestiscono più entità con un livello API comune, ad esempio gestione driver. Anche se non è ancora stato implementato, un esempio è il driver ODBC.

    In questo scenario, il livello intermedio diventa in grado di elaborare associazioni di assembly. Per ottenere il driver di associazione specifico della versione, gli editori devono fornire un manifesto e specificare le dipendenze da componenti specifici in tale manifesto. L'applicazione di base non viene associata dinamicamente ai componenti. in fase di esecuzione, gestione driver gestisce le chiamate. Quando il driver ODBC viene chiamato in base alla stringa di connessione, carica il driver appropriato. Crea quindi il contesto di attivazione usando le informazioni nel file manifesto dell'assembly.

    Senza il manifesto, l'azione predefinita per il driver è usare lo stesso contesto specificato dall'applicazione, in questo esempio la versione 2 di MSVCRT. Poiché esiste un manifesto, viene stabilito un contesto di attivazione separato. Quando viene eseguito, il driver ODBC viene associato alla versione 1 dell'assembly MSVCRT.

    Ogni volta che Gestione driver chiama il livello Dispatch, ad esempio per ottenere il set di dati successivo, usa gli assembly appropriati in base al contesto di attivazione. Il frammento di codice seguente illustra questa operazione.

    <dl> HANDLE hActCtx;  
    ULONG \_ PTR ulpCookie;  
    ACTCTX ActCtxToCreate = {...};  
    hActCtx = CreateActCtx(&ActCtxToCreate);  
    ...;  
    if (ActivateActCtx(hActCtx, &ulpCookie))  
    {  
    ...  
    ConnectDb(...);  
    DeactivateActCtx(0, ulpCookie);  
    }  
    ...  
    ReleaseActCtx(hActCtx);  
    </dl>

 

 

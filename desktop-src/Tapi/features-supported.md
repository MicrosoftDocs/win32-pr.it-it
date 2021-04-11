---
description: L'elenco seguente contiene le funzionalità supportate di TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Funzionalità supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226118"
---
# <a name="features-supported"></a><span data-ttu-id="4dcc4-103">Funzionalità supportate</span><span class="sxs-lookup"><span data-stu-id="4dcc4-103">Features Supported</span></span>

<span data-ttu-id="4dcc4-104">L'elenco seguente contiene le funzionalità supportate di TAPI MSP.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-104">The following list contains the TAPI MSP supported features.</span></span>

-   <span data-ttu-id="4dcc4-105">Implementa un MSP che gestisce un singolo indirizzo per ogni istanza del MSP.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-105">Implements an MSP that handles a single address per instance of the MSP.</span></span> <span data-ttu-id="4dcc4-106">Più indirizzi like vengono gestiti creando un'istanza più volte del MSP.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-106">Multiple like addresses are handled by instantiating the MSP multiple times.</span></span> <span data-ttu-id="4dcc4-107">Questo semplifica notevolmente l'implementazione di MSP e delle classi di base.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-107">This greatly simplifies the implementation of the MSP and the base classes.</span></span>
-   <span data-ttu-id="4dcc4-108">Implementa tutte le interfacce MSPI, tra cui [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="4dcc4-108">Implements all the MSPI interfaces, including [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>
-   <span data-ttu-id="4dcc4-109">Implementa terminali statici pronti per l'uso per audio e video.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-109">Implements ready-to-use static terminals for both audio and video.</span></span>
-   <span data-ttu-id="4dcc4-110">Implementa classi di base di terminali generiche.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-110">Implements generic terminal base classes.</span></span> <span data-ttu-id="4dcc4-111">Queste classi di base di terminali vengono usate sia dalle implementazioni del terminale statico indicate sopra che dalle implementazioni dei terminali dinamici disponibili in Termmgr.dll.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-111">These terminal base classes are used by both the above-mentioned static terminal implementations and the implementations of dynamic terminals that are found in Termmgr.dll.</span></span> <span data-ttu-id="4dcc4-112">Il MSP può anche usarli per implementare terminali aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-112">The MSP can also use them to implement additional terminals.</span></span>
-   <span data-ttu-id="4dcc4-113">USA Terminal Manager per gestire i terminali dinamici.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-113">Uses the Terminal Manager to handle dynamic terminals.</span></span> <span data-ttu-id="4dcc4-114">Crea terminali dinamici in un thread di lavoro con un message pump (per liberare le applicazioni console dalla necessità di elaborare i messaggi della finestra per i terminali di rendering video e per semplificare i problemi di sincronizzazione).</span><span class="sxs-lookup"><span data-stu-id="4dcc4-114">Creates dynamic terminals on a worker thread with a message pump (to free console applications from having to process window messages for video render terminals and to simplify synchronization issues).</span></span>
-   <span data-ttu-id="4dcc4-115">Supporta le chiamate che usano un grafico di filtro per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-115">Supports calls that use a filter graph per stream.</span></span>
-   <span data-ttu-id="4dcc4-116">Implementa la gestione degli eventi Graph.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-116">Implements handling of graph events.</span></span>
-   <span data-ttu-id="4dcc4-117">Usa le API del pool di thread, insieme a un thread di lavoro, per gestire gli eventi.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-117">Uses the thread pooling APIs, in conjunction with a worker thread of its own, to handle events.</span></span>
-   <span data-ttu-id="4dcc4-118">Usa le API di traccia di Windows 2000 (originariamente sviluppate per il progetto di routing) insieme alla logica aggiuntiva per fornire un meccanismo di registrazione generico flessibile che può registrare simultaneamente in qualsiasi combinazione dei seguenti elementi: un debugger in modalità utente o kernel; una finestra della console separata con messaggi di log separati da un componente; un file di log.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-118">Uses the tracing APIs of Windows 2000 (originally developed for the Routing project) along with additional logic to provide a flexible, generic logging mechanism that can simultaneously log to any combination of the following: a user or kernel-mode debugger; a separate console window with log messages separated by component; a log file.</span></span>
-   <span data-ttu-id="4dcc4-119">Viene eseguito a thread libero.</span><span class="sxs-lookup"><span data-stu-id="4dcc4-119">Runs free-threaded.</span></span>

 

 

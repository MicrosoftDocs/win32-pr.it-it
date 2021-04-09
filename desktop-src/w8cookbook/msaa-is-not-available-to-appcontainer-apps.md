---
title: MSAA non è disponibile per le app di Windows Store
description: MSAA non è disponibile per le app di Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047497"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a><span data-ttu-id="77dce-103">MSAA non è disponibile per le app di Windows Store</span><span class="sxs-lookup"><span data-stu-id="77dce-103">MSAA is not available to Windows Store apps</span></span>

## <a name="platform"></a><span data-ttu-id="77dce-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="77dce-104">Platform</span></span>

<span data-ttu-id="77dce-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="77dce-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="77dce-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77dce-106">Description</span></span>

<span data-ttu-id="77dce-107">Windows 8 non supporta MSAA (Microsoft Active Accessibility) per la lettura o l'automazione dei dati accessibili dalle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="77dce-107">Windows 8 does not support MSAA (Microsoft Active Accessibility) for reading or automating accessible data from Windows Store apps.</span></span> <span data-ttu-id="77dce-108">È consigliabile usare l'API di automazione interfaccia utente (UIA), disponibile a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="77dce-108">The UI Automation (UIA) API, available since Windows 7, should be used instead.</span></span> <span data-ttu-id="77dce-109">Poiché non sono presenti funzionalità di app di Windows Store, non sono presenti implementazioni che sono interessate da questa modifica.</span><span class="sxs-lookup"><span data-stu-id="77dce-109">Since there are no existing Windows Store app features, there are no existing implementations that are affected by this change.</span></span> <span data-ttu-id="77dce-110">Questa operazione ha effetto solo sulle nuove app e funzionalità scritte per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77dce-110">This affects only new apps and features written for Windows 8.</span></span> <span data-ttu-id="77dce-111">Gli sviluppatori possono comunque utilizzare MSAA per esporre i propri dati di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="77dce-111">Developers can still use MSAA to expose their accessibility data.</span></span> <span data-ttu-id="77dce-112">Se i dati MSAA sono forniti dal provider di app di Windows Store, i client di UIA saranno comunque in grado di leggere e automatizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="77dce-112">If MSAA data is provided by Windows Store app provider, UIA clients will still be able to read and automate the data.</span></span>

<span data-ttu-id="77dce-113">Per semplificare l'API per le app di Windows Store 8Windows, abbiamo deciso di supportare solo l'automazione dell'interfaccia utente come client per queste app.</span><span class="sxs-lookup"><span data-stu-id="77dce-113">To simplify the API for Windows 8Windows Store apps, we decided to support only UI Automation as a client for these apps.</span></span> <span data-ttu-id="77dce-114">I client di UIA possono leggere i provider UIA in modo nativo, senza alcuna conversione.</span><span class="sxs-lookup"><span data-stu-id="77dce-114">UIA clients can read UIA providers natively, with no translation.</span></span> <span data-ttu-id="77dce-115">I client di UIA possono leggere i provider MSAA come tradotti tramite il proxy UIA-to-MSAA.</span><span class="sxs-lookup"><span data-stu-id="77dce-115">UIA clients can read MSAA providers as translated through the UIA-to-MSAA Proxy.</span></span> <span data-ttu-id="77dce-116">Questo consente di ridurre il carico di test per gli sviluppatori di app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="77dce-116">This will reduce the testing burden for Windows Store app developers.</span></span>

<span data-ttu-id="77dce-117">L'eliminazione del supporto per i provider MSAA ridurrebbe ulteriormente la matrice di test, ma sono presenti app principali ancora basate su MSAA e non si desidera renderle inaccessibili.</span><span class="sxs-lookup"><span data-stu-id="77dce-117">Eliminating support for MSAA providers would further reduce the testing matrix, but there are major apps that are still MSAA-based and we do not want to render them inaccessible.</span></span>

## <a name="manifestation"></a><span data-ttu-id="77dce-118">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="77dce-118">Manifestation</span></span>

<span data-ttu-id="77dce-119">Gli sviluppatori di app di Windows Store non saranno in grado di accedere ai dettagli di MSAA all'interno del modello di app.</span><span class="sxs-lookup"><span data-stu-id="77dce-119">Windows Store app developers will not be able to access the details of MSAA within the app model.</span></span>

## <a name="solution"></a><span data-ttu-id="77dce-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="77dce-120">Solution</span></span>

<span data-ttu-id="77dce-121">Non è necessario creare nuovi casi automatizzati in MSAA per le funzionalità delle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="77dce-121">No new automated cases should be authored in MSAA for features of Windows Store apps.</span></span>

<span data-ttu-id="77dce-122">Se è necessario interagire con le app di Windows Store, è possibile cambiare tutti gli strumenti predefiniti esistenti che usano MSAA in UIA.</span><span class="sxs-lookup"><span data-stu-id="77dce-122">Switch any existing in-box tools that use MSAA to UIA if they need to interact with Windows Store apps.</span></span> <span data-ttu-id="77dce-123">Gli sviluppatori di app di Windows Store devono usare l'API di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="77dce-123">Windows Store app developers should use the UI Automation API.</span></span>

## <a name="resources"></a><span data-ttu-id="77dce-124">Risorse</span><span class="sxs-lookup"><span data-stu-id="77dce-124">Resources</span></span>

-   [<span data-ttu-id="77dce-125">Nozioni fondamentali sull'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="77dce-125">UI Automation Fundamentals</span></span>](../winauto/entry-uiauto-win32.md)

 

 
---
title: DPI elevato per le app desktop in Windows 8.1
description: DPI elevato per le app desktop in Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300054"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a><span data-ttu-id="7ef73-103">DPI elevato per le app desktop in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7ef73-103">High DPI for desktop apps in Windows 8.1</span></span>

## <a name="platforms"></a><span data-ttu-id="7ef73-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="7ef73-104">Platforms</span></span>

<dl> <span data-ttu-id="7ef73-105">Client-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7ef73-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="7ef73-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7ef73-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="7ef73-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ef73-107">Description</span></span>

<span data-ttu-id="7ef73-108">In Windows 8.1 le applicazioni desktop dovrebbero essere eseguite su schermi con scalabilità del 200% oltre alla scalabilità 100%, 125% e 150% supportata in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7ef73-108">In Windows 8.1 desktop applications are expected to run on displays with 200% scaling in addition to the 100%, 125%, and 150% scaling that is supported in Windows 8.</span></span> <span data-ttu-id="7ef73-109">Inoltre, le applicazioni desktop vengono ridimensionate in base al monitoraggio anziché a un singolo fattore di scala applicato a tutte le visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="7ef73-109">In addition, desktop applications are scaled on a per-monitor basis rather than to a single scale factor applied to all displays.</span></span> <span data-ttu-id="7ef73-110">Gli sviluppatori possono anche chiamare le nuove API in Windows 8.1 per ottenere i fattori di scala per monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7ef73-110">Developers can also call new APIs in Windows 8.1 to get per-monitor scale factors.</span></span>

## <a name="manifestations"></a><span data-ttu-id="7ef73-111">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="7ef73-111">Manifestations</span></span>

<span data-ttu-id="7ef73-112">Gli utenti possono usare nuovi schermi ad alta densità con Windows 8.1 per un'esperienza visiva eccezionale che sfrutta i vantaggi dei dati pixel più elevati.</span><span class="sxs-lookup"><span data-stu-id="7ef73-112">Users can use new high density displays with Windows 8.1 for a terrific visual experience that takes advantage of the higher pixel data.</span></span> <span data-ttu-id="7ef73-113">Se le applicazioni non gestiscono valori DPI alti, Windows ne eseguirà la scalabilità per l'utente.</span><span class="sxs-lookup"><span data-stu-id="7ef73-113">If applications don’t handle high DPI, Windows will scale them for the user.</span></span> <span data-ttu-id="7ef73-114">Inoltre, gli utenti possono usare una combinazione di schermi ad alta e bassa densità sullo stesso computer e Windows ridimensiona il contenuto in modo appropriato per ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7ef73-114">In addition, users can use a mix of high and low density displays on the same computer, and Windows will scale content appropriately for each display.</span></span> <span data-ttu-id="7ef73-115">Si tratta di un miglioramento rispetto a Windows 8, in cui il contenuto può essere troppo grande in alcune visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="7ef73-115">This is an improvement over Windows 8, where content can be too large on some displays.</span></span>

## <a name="mitigation"></a><span data-ttu-id="7ef73-116">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="7ef73-116">Mitigation</span></span>

<span data-ttu-id="7ef73-117">Poiché Windows ridimensiona le app che non si ridimensionano, gli sviluppatori in genere non sono in grado di eseguire altre attività, ma gli sviluppatori che investono nella scrittura di applicazioni che supportano valori DPI elevati avranno un vantaggio competitivo, dal momento che tali applicazioni avranno un aspetto migliore sui nuovi computer con DPI e i monitor desktop a risoluzione elevata.</span><span class="sxs-lookup"><span data-stu-id="7ef73-117">Since Windows will scale apps that don’t scale themselves, developers generally do not have to do additional work, but developers who do invest in writing applications that support high DPI will have a competitive advantage, as those applications will look better on new high DPI laptops and desktop monitors.</span></span>

## <a name="solution"></a><span data-ttu-id="7ef73-118">Soluzione</span><span class="sxs-lookup"><span data-stu-id="7ef73-118">Solution</span></span>

<span data-ttu-id="7ef73-119">La creazione di un'applicazione in grado di sfruttare i vantaggi di DPI elevati è un'attività di progettazione e implementazione complessa.</span><span class="sxs-lookup"><span data-stu-id="7ef73-119">Making an application that can take advantage of high DPI is a complex design and implementation task.</span></span> <span data-ttu-id="7ef73-120">Vedere i collegamenti seguenti per informazioni sull'esercitazione, compilare contenuto della presentazione e supporto analogo.</span><span class="sxs-lookup"><span data-stu-id="7ef73-120">See the links below for tutorial information, BUILD presentation content, and similar support.</span></span>

## <a name="tests"></a><span data-ttu-id="7ef73-121">Test</span><span class="sxs-lookup"><span data-stu-id="7ef73-121">Tests</span></span>

<span data-ttu-id="7ef73-122">Anche se gli sviluppatori non scelgono di sfruttare i vantaggi del valore DPI elevato, devono testare l'applicazione in base al 100%, al 125%, al 150% e al 200% di ridimensionamento per assicurarsi che l'esperienza dell'utente finale sia soddisfacente e competitiva.</span><span class="sxs-lookup"><span data-stu-id="7ef73-122">Even if developers do not choose to make their applications take advantage of high DPI, they should test their application at 100%, 125%, 150%, and 200% scaling to be sure the end-user experience is satisfactory and competitive.</span></span>

## <a name="resources"></a><span data-ttu-id="7ef73-123">Risorse</span><span class="sxs-lookup"><span data-stu-id="7ef73-123">Resources</span></span>

-   [<span data-ttu-id="7ef73-124">White paper e Esercitazione su DPI alti in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7ef73-124">White paper and tutorial on high DPI in Windows 8.1</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [<span data-ttu-id="7ef73-125">Programmi di esempio per desktop Windows</span><span class="sxs-lookup"><span data-stu-id="7ef73-125">Windows desktop sample programs</span></span>](https://www.microsoft.com/?ref=go)
-   [<span data-ttu-id="7ef73-126">COMPILAZIONE della sessione di break-out 2013 su DPI elevato in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7ef73-126">BUILD 2013 break-out session on high DPI in Windows 8.1</span></span>](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 
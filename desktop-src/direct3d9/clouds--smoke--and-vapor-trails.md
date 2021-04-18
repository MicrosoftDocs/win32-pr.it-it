---
description: Gli itinerari cloud, fumo e Vapor possono essere creati da un'estensione della tecnica di Billboard.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Percorsi cloud, fumo e Vapor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570440"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a><span data-ttu-id="9d853-103">Percorsi cloud, fumo e Vapor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9d853-103">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>

<span data-ttu-id="9d853-104">Gli itinerari cloud, fumo e Vapor possono essere creati da un'estensione della tecnica di Billboard.</span><span class="sxs-lookup"><span data-stu-id="9d853-104">Clouds, smoke, and vapor trails can all be created by an extension of the billboarding technique.</span></span> <span data-ttu-id="9d853-105">Vedere la pagina relativa al [tabellone (Direct3D 9)](billboarding.md).</span><span class="sxs-lookup"><span data-stu-id="9d853-105">See [Billboarding (Direct3D 9)](billboarding.md).</span></span> <span data-ttu-id="9d853-106">Ruotando il tabellone in due assi anziché uno, l'applicazione può consentire all'utente di visualizzare un tabellone da qualsiasi angolo.</span><span class="sxs-lookup"><span data-stu-id="9d853-106">By rotating the billboard on two axes instead of one, your application can enable the user to view a billboard from any angle.</span></span> <span data-ttu-id="9d853-107">In genere, un'applicazione ruota il tabellone sugli assi orizzontali e verticali.</span><span class="sxs-lookup"><span data-stu-id="9d853-107">Typically, an application rotates the billboard on the horizontal and vertical axes.</span></span>

<span data-ttu-id="9d853-108">Per creare un cloud semplice, l'applicazione può ruotare una primitiva rettangolare su uno o due assi in modo che la primitiva faccia fronte all'utente.</span><span class="sxs-lookup"><span data-stu-id="9d853-108">To make a simple cloud, your application can rotate a rectangular primitive on one or two axes so that the primitive faces the user.</span></span> <span data-ttu-id="9d853-109">Una trama simile al cloud può quindi essere applicata alla primitiva con trasparenza.</span><span class="sxs-lookup"><span data-stu-id="9d853-109">A cloud-like texture can then be applied to the primitive with transparency.</span></span> <span data-ttu-id="9d853-110">Per informazioni dettagliate sull'applicazione di trame trasparenti alle primitive, vedere [blending delle trame (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="9d853-110">For details on applying transparent textures to primitives, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="9d853-111">È possibile aggiungere un'animazione al cloud applicando una serie di trame nel tempo.</span><span class="sxs-lookup"><span data-stu-id="9d853-111">You can animate the cloud by applying a series of textures over time.</span></span>

<span data-ttu-id="9d853-112">Un'applicazione può creare cloud più complessi creandoli da un gruppo di primitive.</span><span class="sxs-lookup"><span data-stu-id="9d853-112">An application can create more complex clouds by forming them from a group of primitives.</span></span> <span data-ttu-id="9d853-113">Ogni parte del cloud è una primitiva rettangolare.</span><span class="sxs-lookup"><span data-stu-id="9d853-113">Each part of the cloud is a rectangular primitive.</span></span> <span data-ttu-id="9d853-114">Le primitive possono essere spostate in modo indipendente nel tempo per dare l'impressione di una nebbia dinamica.</span><span class="sxs-lookup"><span data-stu-id="9d853-114">The primitives can be moved independently over time to give the appearance of a dynamic mist.</span></span> <span data-ttu-id="9d853-115">Nella figura seguente viene illustrato questo concetto.</span><span class="sxs-lookup"><span data-stu-id="9d853-115">The following illustration shows this concept.</span></span>

![illustrazione di primitive che formano cloud più complessi](images/cloud.png)

<span data-ttu-id="9d853-117">L'aspetto del fumo viene visualizzato in modo analogo ai cloud.</span><span class="sxs-lookup"><span data-stu-id="9d853-117">The appearance of smoke is displayed in a manner similar to clouds.</span></span> <span data-ttu-id="9d853-118">Richiede in genere più cartelloni, ad esempio cloud complessi.</span><span class="sxs-lookup"><span data-stu-id="9d853-118">It typically requires multiple billboards, like complex clouds.</span></span> <span data-ttu-id="9d853-119">Un fumo in genere fluttua e aumenta nel tempo, quindi i tabelloni che compongono il fumo devono essere spostati di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="9d853-119">Smoke usually billows and rises over time, so the billboards that make up the smoke plume need to move accordingly.</span></span> <span data-ttu-id="9d853-120">Potrebbe essere necessario aggiungere più tabelloni quando il pennacchio aumenta e si disperde.</span><span class="sxs-lookup"><span data-stu-id="9d853-120">You may need to add more billboards as the plume rises and disperses.</span></span>

<span data-ttu-id="9d853-121">Una pista di vapore è un fumo che non aumenta.</span><span class="sxs-lookup"><span data-stu-id="9d853-121">A vapor trail is a smoke plume that doesn't rise.</span></span> <span data-ttu-id="9d853-122">Tuttavia, come un pennacchio di fumo, si disperde nel tempo.</span><span class="sxs-lookup"><span data-stu-id="9d853-122">However, like a smoke plume, it disperses over time.</span></span> <span data-ttu-id="9d853-123">Nella figura seguente viene illustrata la tecnica di utilizzo dei tabelloni per simulare una pista di vapori.</span><span class="sxs-lookup"><span data-stu-id="9d853-123">The following illustration shows the technique of using billboards to simulate a vapor trail.</span></span>

![illustrazione dei tabelloni che simulano una pista di vapore](images/vapor.png)

## <a name="related-topics"></a><span data-ttu-id="9d853-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d853-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d853-126">Esempi di Alpha</span><span class="sxs-lookup"><span data-stu-id="9d853-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 




---
title: Informazioni su Direct3D 12
description: Per scrivere giochi 3D e app per Windows 10 e Windows 10 Mobile, è necessario comprendere le nozioni di base della tecnologia Direct3D 12 e come prepararsi a usarla nei giochi e nelle app.
ms.assetid: DED7A434-FCD4-4F41-8B2C-E5AE6E48430F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1353c8c66fd401e364b9db302463f164f757c9ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548893"
---
# <a name="understanding-direct3d-12"></a><span data-ttu-id="faedc-103">Informazioni su Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="faedc-103">Understanding Direct3D 12</span></span>

<span data-ttu-id="faedc-104">Per scrivere giochi 3D e app per Windows 10 e Windows 10 Mobile, è necessario comprendere le nozioni di base della tecnologia Direct3D 12 e come prepararsi a usarla nei giochi e nelle app.</span><span class="sxs-lookup"><span data-stu-id="faedc-104">To write 3D games and apps for Windows 10 and Windows 10 Mobile, you must understand the basics of the Direct3D 12 technology, and how to prepare to use it in your games and apps.</span></span>

<span data-ttu-id="faedc-105">Usare gli argomenti di questa sezione per configurare e ottenere informazioni sull'ambiente in cui si prevede di programmare le app e i giochi con Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="faedc-105">Use the topics in this section to set up and learn about the environment in which you will program your apps and games with Direct3D 12.</span></span> <span data-ttu-id="faedc-106">Questo contenuto ti aiuterà anche a trasferire app e giochi Direct3D 11 a Direct3D 12, per poter sfruttare le funzionalità e le efficienze di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="faedc-106">This content will also help you to port your Direct3D 11 apps and games to Direct3D 12, so you can take advantage of Direct3D 12 features and efficiencies.</span></span>

<span data-ttu-id="faedc-107">Per programmare con Direct3D 12, sono necessari i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="faedc-107">To program with Direct3D 12, you need these components:</span></span>

-   <span data-ttu-id="faedc-108">Una piattaforma hardware con una GPU compatibile con Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="faedc-108">A hardware platform with a Direct3D 12-compatible GPU</span></span>
-   <span data-ttu-id="faedc-109">[Visualizza driver](/previous-versions//ff569172(v=vs.85)) che supportano Windows Display Driver Model (WDDM) 2,0</span><span class="sxs-lookup"><span data-stu-id="faedc-109">[Display drivers](/previous-versions//ff569172(v=vs.85)) that support the Windows Display Driver Model (WDDM) 2.0</span></span>

## <a name="in-this-section"></a><span data-ttu-id="faedc-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="faedc-110">In this section</span></span>



| <span data-ttu-id="faedc-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="faedc-111">Topic</span></span>                                                                                                               | <span data-ttu-id="faedc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faedc-112">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="faedc-113">Configurazione dell'ambiente di programmazione Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="faedc-113">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)<br/>               | <span data-ttu-id="faedc-114">Descrive l'installazione, gli strumenti e le librerie supportate che costituiscono un ambiente di sviluppo Direct3D 12 produttivo.</span><span class="sxs-lookup"><span data-stu-id="faedc-114">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span> <br/>                              |
| [<span data-ttu-id="faedc-115">Creazione di un componente Direct3D 12 di base</span><span class="sxs-lookup"><span data-stu-id="faedc-115">Creating a Basic Direct3D 12 Component</span></span>](creating-a-basic-direct3d-12-component.md)<br/>                     | <span data-ttu-id="faedc-116">In questo argomento viene descritto il flusso di chiamate per creare un componente Direct3D 12 di base.</span><span class="sxs-lookup"><span data-stu-id="faedc-116">This topic describes the call flow to create a basic Direct3D 12 component.</span></span><br/>                                                                            |
| [<span data-ttu-id="faedc-117">Modifiche importanti da Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="faedc-117">Important Changes from Direct3D 11 to Direct3D 12</span></span>](important-changes-from-directx-11-to-directx-12.md)<br/> | <span data-ttu-id="faedc-118">Direct3D 12 rappresenta una partenza significativa dal modello di programmazione Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="faedc-118">Direct3D 12 represents a significant departure from the Direct3D 11 programming model.</span></span> <span data-ttu-id="faedc-119">Direct3D 12 consente alle app di avvicinarsi a hardware che mai.</span><span class="sxs-lookup"><span data-stu-id="faedc-119">Direct3D 12 lets apps get closer to hardware than ever before.</span></span> <br/> |
| [<span data-ttu-id="faedc-120">Livelli di funzionalità hardware</span><span class="sxs-lookup"><span data-stu-id="faedc-120">Hardware Feature Levels</span></span>](hardware-feature-levels.md)<br/>                                                   | <span data-ttu-id="faedc-121">Descrive la funzionalità dei livelli di \_ funzionalità hardware da 11 a 12 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="faedc-121">Describes the functionality of the 11\_0 through 12\_1 hardware feature levels.</span></span><br/>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="faedc-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="faedc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faedc-123">Guida per programmatori Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="faedc-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 


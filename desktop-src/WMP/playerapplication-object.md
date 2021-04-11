---
title: Oggetto PlayerApplication
description: L'oggetto PlayerApplication fornisce un modo per coordinare il passaggio tra un controllo Media Player Windows remoto e la modalità completa di Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Media Player di Windows oggetto PlayerApplication
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104334951"
---
# <a name="playerapplication-object"></a><span data-ttu-id="e1e00-104">Oggetto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="e1e00-104">PlayerApplication Object</span></span>

<span data-ttu-id="e1e00-105">L'oggetto **PlayerApplication** fornisce un modo per coordinare il passaggio tra un controllo Media Player Windows remoto e la modalità completa di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e1e00-105">The **PlayerApplication** object provides a way to coordinate switching between a remoted Windows Media Player control and the full mode of Windows Media Player.</span></span> <span data-ttu-id="e1e00-106">Questo oggetto viene usato solo con i programmi C++ che implementano l'interfaccia **IWMPRemoteMediaServices** e incorporano il controllo Player in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="e1e00-106">This object is used only with C++ programs that implement the **IWMPRemoteMediaServices** interface and embed the Player control in remote mode.</span></span> <span data-ttu-id="e1e00-107">I file di interfaccia usati come interfacce personalizzate per il controllo Windows Media Player remoto accedono a questo oggetto nel codice di script tramite l'attributo globale **playerApplication** .</span><span class="sxs-lookup"><span data-stu-id="e1e00-107">Skin files used as custom interfaces for the remoted Windows Media Player control access this object in script code through the **playerApplication** global attribute.</span></span>

<span data-ttu-id="e1e00-108">L'oggetto **PlayerApplication** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="e1e00-108">The **PlayerApplication** object supports the following properties.</span></span>



| <span data-ttu-id="e1e00-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1e00-109">Property</span></span>                                           | <span data-ttu-id="e1e00-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1e00-110">Description</span></span>                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1e00-111">hasDisplay</span><span class="sxs-lookup"><span data-stu-id="e1e00-111">hasDisplay</span></span>](playerapplication-hasdisplay.md)     | <span data-ttu-id="e1e00-112">Recupera un valore che indica se il video può essere visualizzato tramite il controllo Media Player remoto di Windows.</span><span class="sxs-lookup"><span data-stu-id="e1e00-112">Retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span> |
| [<span data-ttu-id="e1e00-113">playerDocked</span><span class="sxs-lookup"><span data-stu-id="e1e00-113">playerDocked</span></span>](playerapplication-playerdocked.md) | <span data-ttu-id="e1e00-114">Recupera un valore che indica se Windows Media Player si trova in uno stato ancorato.</span><span class="sxs-lookup"><span data-stu-id="e1e00-114">Retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>                          |



 

<span data-ttu-id="e1e00-115">L'oggetto **PlayerApplication** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e1e00-115">The **PlayerApplication** object supports the following methods.</span></span>



| <span data-ttu-id="e1e00-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="e1e00-116">Method</span></span>                                                                       | <span data-ttu-id="e1e00-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1e00-117">Description</span></span>                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="e1e00-118">switchToControl</span><span class="sxs-lookup"><span data-stu-id="e1e00-118">switchToControl</span></span>](playerapplication-switchtocontrol.md)                     | <span data-ttu-id="e1e00-119">Passa un controllo Media Player Windows remoto allo stato ancorato.</span><span class="sxs-lookup"><span data-stu-id="e1e00-119">Switches a remoted Windows Media Player control to the docked state.</span></span>            |
| [<span data-ttu-id="e1e00-120">switchToPlayerApplication</span><span class="sxs-lookup"><span data-stu-id="e1e00-120">switchToPlayerApplication</span></span>](playerapplication-switchtoplayerapplication.md) | <span data-ttu-id="e1e00-121">Passa un controllo Media Player Windows remoto alla modalità completa del lettore.</span><span class="sxs-lookup"><span data-stu-id="e1e00-121">Switches a remoted Windows Media Player control to the full mode of the Player.</span></span> |



 

<span data-ttu-id="e1e00-122">È possibile accedere all'oggetto **PlayerApplication** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="e1e00-122">The **PlayerApplication** object is accessed through the following property.</span></span>



| <span data-ttu-id="e1e00-123">Oggetto</span><span class="sxs-lookup"><span data-stu-id="e1e00-123">Object</span></span>                      | <span data-ttu-id="e1e00-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1e00-124">Property</span></span>                                          |
|-----------------------------|---------------------------------------------------|
| [<span data-ttu-id="e1e00-125">Player</span><span class="sxs-lookup"><span data-stu-id="e1e00-125">Player</span></span>](player-object.md) | [<span data-ttu-id="e1e00-126">playerApplication</span><span class="sxs-lookup"><span data-stu-id="e1e00-126">playerApplication</span></span>](player-playerapplication.md) |



 

## <a name="see-also"></a><span data-ttu-id="e1e00-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1e00-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1e00-128">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="e1e00-128">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="e1e00-129">**Gestione remota del controllo di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="e1e00-129">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





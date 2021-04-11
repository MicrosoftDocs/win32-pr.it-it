---
title: Oggetto cdrom
description: L'oggetto cdrom fornisce un modo per accedere a un CD o DVD nell'unità.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Media Player di Windows per oggetti cdrom
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333191"
---
# <a name="cdrom-object"></a><span data-ttu-id="fd530-104">Oggetto cdrom</span><span class="sxs-lookup"><span data-stu-id="fd530-104">Cdrom Object</span></span>

<span data-ttu-id="fd530-105">L'oggetto **CDROM** fornisce un modo per accedere a un CD o DVD nell'unità.</span><span class="sxs-lookup"><span data-stu-id="fd530-105">The **Cdrom** object provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="fd530-106">L'oggetto **CDROM** supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd530-106">The **Cdrom** object supports the following properties.</span></span>



| <span data-ttu-id="fd530-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd530-107">Property</span></span>                                   | <span data-ttu-id="fd530-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd530-108">Description</span></span>                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd530-109">driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="fd530-109">driveSpecifier</span></span>](cdrom-drivespecifier.md) | <span data-ttu-id="fd530-110">Recupera la lettera dell'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="fd530-110">Retrieves the CD or DVD drive letter.</span></span>                                                                                                                   |
| [<span data-ttu-id="fd530-111">playlist</span><span class="sxs-lookup"><span data-stu-id="fd530-111">playlist</span></span>](cdrom-playlist.md)             | <span data-ttu-id="fd530-112">Recupera un oggetto [playlist](playlist-object.md) che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per DVD.</span><span class="sxs-lookup"><span data-stu-id="fd530-112">Retrieves a [Playlist](playlist-object.md) object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span> |



 

<span data-ttu-id="fd530-113">L'oggetto **CDROM** supporta il seguente metodo.</span><span class="sxs-lookup"><span data-stu-id="fd530-113">The **Cdrom** object supports the following method.</span></span>



| <span data-ttu-id="fd530-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="fd530-114">Method</span></span>                   | <span data-ttu-id="fd530-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd530-115">Description</span></span>                          |
|--------------------------|--------------------------------------|
| [<span data-ttu-id="fd530-116">Eject</span><span class="sxs-lookup"><span data-stu-id="fd530-116">eject</span></span>](cdrom-eject.md) | <span data-ttu-id="fd530-117">Espelle il CD o il DVD dall'unità.</span><span class="sxs-lookup"><span data-stu-id="fd530-117">Ejects the CD or DVD from the drive.</span></span> |



 

<span data-ttu-id="fd530-118">È possibile accedere all'oggetto **CDROM** tramite il metodo seguente.</span><span class="sxs-lookup"><span data-stu-id="fd530-118">The **Cdrom** object is accessed through the following method.</span></span>



| <span data-ttu-id="fd530-119">Oggetto</span><span class="sxs-lookup"><span data-stu-id="fd530-119">Object</span></span>                                        | <span data-ttu-id="fd530-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="fd530-120">Method</span></span>                           |
|-----------------------------------------------|----------------------------------|
| [<span data-ttu-id="fd530-121">Cdromcollection</span><span class="sxs-lookup"><span data-stu-id="fd530-121">CdromCollection</span></span>](cdromcollection-object.md) | [<span data-ttu-id="fd530-122">item</span><span class="sxs-lookup"><span data-stu-id="fd530-122">item</span></span>](cdromcollection-item.md) |



 

<span data-ttu-id="fd530-123">Ai fini dell'illustrazione, Player. cdromCollection. Item (*index*) viene usato nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="fd530-123">For purposes of illustration, player.cdromCollection.item(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd530-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd530-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd530-125">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="fd530-125">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





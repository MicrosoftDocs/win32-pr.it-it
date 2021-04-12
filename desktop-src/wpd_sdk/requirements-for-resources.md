---
description: Requisiti per le risorse
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Requisiti per le risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232693"
---
# <a name="requirements-for-resources"></a><span data-ttu-id="c36ba-103">Requisiti per le risorse</span><span class="sxs-lookup"><span data-stu-id="c36ba-103">Requirements for Resources</span></span>

<span data-ttu-id="c36ba-104">I dispositivi portatili Windows definiscono le seguenti categorie di risorse come valori **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="c36ba-104">Windows Portable Devices defines the following resource categories as **PROPERTYKEY** values.</span></span> <span data-ttu-id="c36ba-105">Questi valori vengono utilizzati per descrivere le singole risorse in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c36ba-105">These values are used to describe individual resources in an object.</span></span> <span data-ttu-id="c36ba-106">Il membro *PID* della chiave della proprietà può essere diverso per descrivere risorse diverse dello stesso tipo per tutti i tipi ad eccezione di **WPD \_ Resource \_ default**, che può descrivere solo una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c36ba-106">The *pid* member of the property key can be different to describe different resources of the same type for all types except **WPD\_RESOURCE\_DEFAULT**, which can only describe one resource.</span></span> <span data-ttu-id="c36ba-107">La pagina di descrizione collegata per ogni tipo di risorsa elenca gli attributi supportati da tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="c36ba-107">The linked description page for each resource type lists the attributes supported by that resource.</span></span>



| <span data-ttu-id="c36ba-108">PROPERTYKEY risorse</span><span class="sxs-lookup"><span data-stu-id="c36ba-108">Resource PROPERTYKEY</span></span>                                                | <span data-ttu-id="c36ba-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c36ba-109">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c36ba-110">**\_impostazione predefinita della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c36ba-110">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)              | <span data-ttu-id="c36ba-111">Specifica l'intero file sottostante l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c36ba-111">Specifies the whole file behind the object.</span></span> <span data-ttu-id="c36ba-112">Questa è l'unica risorsa necessaria per qualsiasi oggetto con una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c36ba-112">This is the only required resource for any object with a resource.</span></span> |
| [<span data-ttu-id="c36ba-113">**\_Art album delle risorse WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c36ba-113">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md)         | <span data-ttu-id="c36ba-114">Specifica un'immagine che rappresenta la grafica dell'album per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c36ba-114">Specifies an image that represents the album artwork for the object.</span></span>                                           |
| [<span data-ttu-id="c36ba-115">**\_ \_ clip audio della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c36ba-115">**WPD\_RESOURCE\_AUDIO\_CLIP**</span></span>](wpd-resource-audio-clip.md)       | <span data-ttu-id="c36ba-116">Specifica un clip audio per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c36ba-116">Specifies an audio clip for the object.</span></span>                                                                        |
| [<span data-ttu-id="c36ba-117">**\_ \_ Foto contatto risorse \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c36ba-117">**WPD\_RESOURCE\_CONTACT\_PHOTO**</span></span>](wpd-resource-contact-photo.md) | <span data-ttu-id="c36ba-118">Specifica un'immagine che rappresenta una foto dell'utente a cui si fa riferimento nell'oggetto contatto.</span><span class="sxs-lookup"><span data-stu-id="c36ba-118">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>                |
| [<span data-ttu-id="c36ba-119">**\_risorsa WPD \_ generica**</span><span class="sxs-lookup"><span data-stu-id="c36ba-119">**WPD\_RESOURCE\_GENERIC**</span></span>](wpd-resource-generic.md)              | <span data-ttu-id="c36ba-120">Una risorsa generica del tipo di dati non definito.</span><span class="sxs-lookup"><span data-stu-id="c36ba-120">A generic resource of undefined data type.</span></span> <span data-ttu-id="c36ba-121">Questa operazione deve essere considerata come una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="c36ba-121">This should be treated as a byte array.</span></span>                             |
| [<span data-ttu-id="c36ba-122">**\_icona della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c36ba-122">**WPD\_RESOURCE\_ICON**</span></span>](wpd-resource-icon.md)                    | <span data-ttu-id="c36ba-123">Un'icona.</span><span class="sxs-lookup"><span data-stu-id="c36ba-123">An icon.</span></span>                                                                                                       |
| [<span data-ttu-id="c36ba-124">**\_anteprima della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c36ba-124">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)          | <span data-ttu-id="c36ba-125">Immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="c36ba-125">A thumbnail image.</span></span>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="c36ba-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c36ba-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c36ba-127">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="c36ba-127">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




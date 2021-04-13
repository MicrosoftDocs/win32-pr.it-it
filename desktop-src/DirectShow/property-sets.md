---
description: Set di proprietà
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Set di proprietà (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401179"
---
# <a name="property-sets-directshow"></a><span data-ttu-id="02039-103">Set di proprietà (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="02039-103">Property Sets (DirectShow)</span></span>

<span data-ttu-id="02039-104">Microsoft DirectShow usa i set di proprietà per supportare i servizi estesi offerti dall'hardware e i relativi driver e filtri associati.</span><span class="sxs-lookup"><span data-stu-id="02039-104">Microsoft DirectShow uses property sets to support extended services offered by hardware and its associated drivers and filters.</span></span> <span data-ttu-id="02039-105">I fornitori di hardware e filtri possono definire nuove funzionalità come proprietà, disporli in set di proprietà e pubblicare la specifica per questi set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="02039-105">Hardware and filter vendors can define new capabilities as properties, arrange them in property sets, and publish the specification for these property sets.</span></span> <span data-ttu-id="02039-106">Lo sviluppatore di applicazioni può utilizzare i metodi dell'interfaccia [**IKsPropertySet**](ikspropertyset.md) per determinare se un driver o un filtro supporta un determinato set di proprietà e recuperare o impostare tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="02039-106">As the application developer, you can use the methods of the [**IKsPropertySet**](ikspropertyset.md) interface to determine whether a driver or filter supports a particular set of properties, and retrieve or set those properties.</span></span>

<span data-ttu-id="02039-107">Tutti i metodi esposti da **IKsPropertySet** richiedono un **GUID** che identifichi il set di proprietà (parametro *GuidPropSet* ) e un **valore DWORD** che identifica la proprietà all'interno del set di proprietà (parametro *dwPropID* ).</span><span class="sxs-lookup"><span data-stu-id="02039-107">All the methods exposed by **IKsPropertySet** require a **GUID** that identifies the property set (the *guidPropSet* parameter) and a **DWORD** that identifies the property within the property set (the *dwPropID* parameter).</span></span> <span data-ttu-id="02039-108">Il parametro *dwPropID* è in genere un membro di un tipo di dati enumerato.</span><span class="sxs-lookup"><span data-stu-id="02039-108">The *dwPropID* parameter is typically a member of an enumerated data type.</span></span>

<span data-ttu-id="02039-109">Le singole proprietà possono avere dati associati specificati nel parametro *pPropData* nei metodi [**IKsPropertySet:: set**](ikspropertyset-set.md) e [**IKsPropertySet:: Get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="02039-109">Individual properties can have associated data that you specify in the *pPropData* parameter in the [**IKsPropertySet::Set**](ikspropertyset-set.md) and [**IKsPropertySet::Get**](ikspropertyset-get.md) methods.</span></span> <span data-ttu-id="02039-110">In questi metodi, i dati della proprietà sono tipizzati come puntatore a `void` .</span><span class="sxs-lookup"><span data-stu-id="02039-110">In these methods, the property data is typed as a pointer to `void`.</span></span> <span data-ttu-id="02039-111">Il tipo di dati e il significato dei dati vengono specificati nella definizione del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="02039-111">The data type and the meaning of the data are specified in the definition of the property set.</span></span>

<span data-ttu-id="02039-112">Le sezioni seguenti forniscono informazioni sui set di proprietà supportati in DirectShow:</span><span class="sxs-lookup"><span data-stu-id="02039-112">The following sections provide information about the property sets supported in DirectShow:</span></span>

-   [<span data-ttu-id="02039-113">**Set di proprietà di protezione copia DVD**</span><span class="sxs-lookup"><span data-stu-id="02039-113">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="02039-114">**Set di proprietà di DVD karaoke**</span><span class="sxs-lookup"><span data-stu-id="02039-114">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="02039-115">**Set di proprietà della sottoimmagine DVD**</span><span class="sxs-lookup"><span data-stu-id="02039-115">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="02039-116">Set di proprietà di trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="02039-116">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
-   [<span data-ttu-id="02039-117">Set di proprietà di avanzamento frame</span><span class="sxs-lookup"><span data-stu-id="02039-117">Frame Stepping Property Set</span></span>](frame-stepping-property-set.md)
-   [<span data-ttu-id="02039-118">Imposta la proprietà pin</span><span class="sxs-lookup"><span data-stu-id="02039-118">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="02039-119">**Set di proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="02039-119">**Rate Change Property Set**</span></span>](rate-change-property-set.md)

 

 




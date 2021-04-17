---
description: Tutti gli oggetti Item dispongono di proprietà.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Attributi di proprietà (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485060"
---
# <a name="property-attributes-wia"></a><span data-ttu-id="d51b9-103">Attributi di proprietà (WIA)</span><span class="sxs-lookup"><span data-stu-id="d51b9-103">Property Attributes (WIA)</span></span>

<span data-ttu-id="d51b9-104">Tutti gli oggetti Item dispongono di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d51b9-104">All item objects have properties.</span></span> <span data-ttu-id="d51b9-105">Le proprietà hanno attributi.</span><span class="sxs-lookup"><span data-stu-id="d51b9-105">The properties have attributes.</span></span> <span data-ttu-id="d51b9-106">Ad esempio, gli attributi delle proprietà indicano se una proprietà viene letta, scritta o eliminata.</span><span class="sxs-lookup"><span data-stu-id="d51b9-106">For instance, property attributes indicate whether a property is read from, written to, or deleted.</span></span> <span data-ttu-id="d51b9-107">Indica inoltre i valori validi della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d51b9-107">They also indicate the valid property values.</span></span> <span data-ttu-id="d51b9-108">Le costanti seguenti sono attributi di proprietà validi:</span><span class="sxs-lookup"><span data-stu-id="d51b9-108">The following constants are valid property attributes:</span></span> 

| <span data-ttu-id="d51b9-109">Attributo Property</span><span class="sxs-lookup"><span data-stu-id="d51b9-109">Property Attribute</span></span>        | <span data-ttu-id="d51b9-110">Significato</span><span class="sxs-lookup"><span data-stu-id="d51b9-110">Meaning</span></span>                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d51b9-111">inseribile \_ \_ nella cache WIA</span><span class="sxs-lookup"><span data-stu-id="d51b9-111">WIA\_PROP\_CACHEABLE</span></span>      | <span data-ttu-id="d51b9-112">Il dispositivo può memorizzare nella cache il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d51b9-112">The device can cache the property's value.</span></span>                                                               |
| <span data-ttu-id="d51b9-113">\_flag di prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="d51b9-113">WIA\_PROP\_FLAG</span></span>           | <span data-ttu-id="d51b9-114">La proprietà dispone di un elenco di valori di flag validi.</span><span class="sxs-lookup"><span data-stu-id="d51b9-114">The property has a list of legal flag values.</span></span> <span data-ttu-id="d51b9-115">I valori dei flag vengono combinati tramite **un'operazione or** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="d51b9-115">Flag values are combined using a bitwise **OR** operation.</span></span> |
| <span data-ttu-id="d51b9-116">\_elenco di oggetti WIA \_</span><span class="sxs-lookup"><span data-stu-id="d51b9-116">WIA\_PROP\_LIST</span></span>           | <span data-ttu-id="d51b9-117">La proprietà dispone di un elenco di valori validi.</span><span class="sxs-lookup"><span data-stu-id="d51b9-117">The property has a list of legal values.</span></span>                                                                 |
| <span data-ttu-id="d51b9-118">\_None Prop \_ nessuno</span><span class="sxs-lookup"><span data-stu-id="d51b9-118">WIA\_PROP\_NONE</span></span>           | <span data-ttu-id="d51b9-119">Alla proprietà non è associato alcun valore valido.</span><span class="sxs-lookup"><span data-stu-id="d51b9-119">The property does not have any valid values associated with it.</span></span>                                          |
| <span data-ttu-id="d51b9-120">\_intervallo di oggetti WIA \_</span><span class="sxs-lookup"><span data-stu-id="d51b9-120">WIA\_PROP\_RANGE</span></span>          | <span data-ttu-id="d51b9-121">La proprietà ha un intervallo di valori validi.</span><span class="sxs-lookup"><span data-stu-id="d51b9-121">The property has a range of valid values.</span></span>                                                                |
| <span data-ttu-id="d51b9-122">\_lettura della prop di WIA \_</span><span class="sxs-lookup"><span data-stu-id="d51b9-122">WIA\_PROP\_READ</span></span>           | <span data-ttu-id="d51b9-123">L'applicazione è in grado di leggere il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d51b9-123">The application can read the property's value.</span></span>                                                           |
| <span data-ttu-id="d51b9-124">WIA \_ prop \_ RW</span><span class="sxs-lookup"><span data-stu-id="d51b9-124">WIA\_PROP\_RW</span></span>             | <span data-ttu-id="d51b9-125">L'applicazione è in grado di leggere e scrivere il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d51b9-125">The application can read and write the property's value.</span></span>                                                 |
| <span data-ttu-id="d51b9-126">\_ \_ richiesta sincronizzazione Prop \_ WIA</span><span class="sxs-lookup"><span data-stu-id="d51b9-126">WIA\_PROP\_SYNC\_REQUIRED</span></span> | <span data-ttu-id="d51b9-127">Non usare.</span><span class="sxs-lookup"><span data-stu-id="d51b9-127">Do not use.</span></span>                                                                                              |
| <span data-ttu-id="d51b9-128">\_scrittura della prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="d51b9-128">WIA\_PROP\_WRITE</span></span>          | <span data-ttu-id="d51b9-129">L'applicazione può scrivere il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d51b9-129">The application can write the property's value.</span></span>                                                          |



 

 

 




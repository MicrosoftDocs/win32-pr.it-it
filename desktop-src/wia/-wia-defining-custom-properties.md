---
description: Definizione di proprietà personalizzate.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definizione di proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312446"
---
# <a name="defining-custom-properties"></a><span data-ttu-id="f7a70-103">Definizione di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="f7a70-103">Defining Custom Properties</span></span>

<span data-ttu-id="f7a70-104">**Definizione di proprietà personalizzate**.</span><span class="sxs-lookup"><span data-stu-id="f7a70-104">**Defining Custom Properties**.</span></span>

<span data-ttu-id="f7a70-105">Se è necessario che Windows Image Acquisition (WIA) minidriver per definire proprietà personalizzate, è necessario usare la \_ \_ Proprietà DEVPROP privata WIA per le proprietà dell'elemento radice personalizzato e la proprietà ITEMPROP (WIA privato) per le proprietà degli \_ \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="f7a70-105">If it is necessary for the Windows Image Acquisition (WIA) minidriver to define custom properties, the WIA\_PRIVATE\_DEVPROP property should be used for custom root item properties, and the WIA\_PRIVATE\_ITEMPROP" property should be used for other item properties.</span></span> <span data-ttu-id="f7a70-106">Queste costanti sono definite in *wiadef. h*.</span><span class="sxs-lookup"><span data-stu-id="f7a70-106">These constants are defined in *wiadef.h*.</span></span>

<span data-ttu-id="f7a70-107">Nell'esempio di codice riportato di seguito vengono illustrate le definizioni per tre proprietà elemento radice.</span><span class="sxs-lookup"><span data-stu-id="f7a70-107">The following example code shows definitions for three root item properties.</span></span> <span data-ttu-id="f7a70-108">L'ID di proprietà della prima proprietà dell'elemento radice personalizzato, \_ ovvero la radice personalizzata \_ \_ 1, è definito in termini \_ di \_ DEVPROP privato WIA.</span><span class="sxs-lookup"><span data-stu-id="f7a70-108">The property ID for the first custom root item property, CUSTOM\_ROOT\_PROP\_1, is defined in terms of WIA\_PRIVATE\_DEVPROP.</span></span> <span data-ttu-id="f7a70-109">Gli ID proprietà per ulteriori proprietà elemento radice sono definiti in termini di WIA \_ privato \_ DEVPROP + 1, WIA \_ privato \_ DEVPROP + 2 e così via.</span><span class="sxs-lookup"><span data-stu-id="f7a70-109">Property IDs for additional root item properties are defined in terms of WIA\_PRIVATE\_DEVPROP + 1, WIA\_PRIVATE\_DEVPROP + 2, and so on.</span></span> <span data-ttu-id="f7a70-110">Il modello può essere continuato se sono necessarie proprietà aggiuntive dell'elemento radice personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f7a70-110">The pattern can be continued if additional custom root item properties are needed.</span></span>


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



<span data-ttu-id="f7a70-111">Nell'esempio seguente vengono illustrate le definizioni per tre proprietà e ID di proprietà degli elementi figlio personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f7a70-111">The next example shows definitions for three custom child item properties and property IDs.</span></span> <span data-ttu-id="f7a70-112">L'ID di proprietà per la prima proprietà elemento figlio personalizzato, l'elemento personalizzato \_ figlio \_ prop \_ 1, viene definito in termini di \_ ITEMPROP privato WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="f7a70-112">The property ID for the first custom child item property, CUSTOM\_CHILD\_PROP\_1, is defined in terms of WIA\_PRIVATE\_ITEMPROP.</span></span> <span data-ttu-id="f7a70-113">Gli ID di proprietà per le proprietà aggiuntive degli elementi figlio sono definiti in termini di WIA \_ privato \_ ITEMPROP + 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="f7a70-113">Property IDs for additional child item properties are defined in terms of WIA\_PRIVATE\_ITEMPROP + 1, and so on.</span></span> <span data-ttu-id="f7a70-114">Come in precedenza, il modello può essere continuato se sono necessarie più proprietà di elemento figlio personalizzate.</span><span class="sxs-lookup"><span data-stu-id="f7a70-114">As before, the pattern can be continued if more of these custom child item properties are needed.</span></span>


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



<span data-ttu-id="f7a70-115">Per le proprietà WIA personalizzate è necessario che i nomi delle proprietà personalizzate siano associati agli ID delle proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="f7a70-115">Custom WIA properties must have custom property names that are associated with the custom property IDs.</span></span> <span data-ttu-id="f7a70-116">Il codice di esempio seguente mostra le definizioni per tre nomi di proprietà dell'elemento radice personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f7a70-116">The following example code shows definitions for three custom root item property names.</span></span> <span data-ttu-id="f7a70-117">Questi nomi di proprietà vengono usati con gli ID di proprietà personalizzati creati in un esempio precedente, in cui il nome della proprietà personalizzata contenuto in CUSTOM \_ \_La radice Prop \_ 1 \_ str è associata alla proprietà dell'elemento radice personalizzato ID della radice personalizzata \_ \_ prop \_ 1.</span><span class="sxs-lookup"><span data-stu-id="f7a70-117">(These property names are used with the custom property IDs that were created in a previous example, where the custom property name contained in CUSTOM\_ROOT\_PROP\_1\_STR is associated with the custom root item property ID CUSTOM\_ROOT\_PROP\_1.)</span></span>


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> <span data-ttu-id="f7a70-118">I nomi di proprietà WIA *non* sono localizzati in più lingue.</span><span class="sxs-lookup"><span data-stu-id="f7a70-118">WIA property names are *not* localized in multiple languages.</span></span> <span data-ttu-id="f7a70-119">Ciò è dovuto al fatto che le proprietà WIA possono essere lette dalle applicazioni utilizzando l'ID proprietà o il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7a70-119">This is because WIA properties can be read by applications using the property ID or the property name.</span></span> <span data-ttu-id="f7a70-120">Se il nome viene usato, deve essere una costante, proprio come l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7a70-120">If the name is used, it must be a constant, just as the property ID is.</span></span>

 

 

 




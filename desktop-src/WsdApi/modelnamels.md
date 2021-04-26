---
description: Specifica una versione localizzata del nome del dispositivo.
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: Elemento modelNameLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47d2f83d1b636efc30e98dff8c46600bcee555d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995498"
---
# <a name="modelnamels-element"></a><span data-ttu-id="ccf22-103">Elemento modelNameLS</span><span class="sxs-lookup"><span data-stu-id="ccf22-103">modelNameLS element</span></span>

<span data-ttu-id="ccf22-104">Specifica una versione localizzata del nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ccf22-104">Specifies a localized version of the device name.</span></span>

## <a name="usage"></a><span data-ttu-id="ccf22-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ccf22-105">Usage</span></span>

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a><span data-ttu-id="ccf22-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="ccf22-106">Attributes</span></span>



| <span data-ttu-id="ccf22-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="ccf22-107">Attribute</span></span>               | <span data-ttu-id="ccf22-108">Type</span><span class="sxs-lookup"><span data-stu-id="ccf22-108">Type</span></span>                                   | <span data-ttu-id="ccf22-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="ccf22-109">Required</span></span>       | <span data-ttu-id="ccf22-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccf22-110">Description</span></span>                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| <span data-ttu-id="ccf22-111">**Dati**</span><span class="sxs-lookup"><span data-stu-id="ccf22-111">**Data**</span></span><br/>     | <span data-ttu-id="ccf22-112">Stringa del nome del modello localizzato</span><span class="sxs-lookup"><span data-stu-id="ccf22-112">localized model name string</span></span><br/> | <span data-ttu-id="ccf22-113">Sì</span><span class="sxs-lookup"><span data-stu-id="ccf22-113">Yes</span></span><br/> | <span data-ttu-id="ccf22-114">Nome del modello localizzato.</span><span class="sxs-lookup"><span data-stu-id="ccf22-114">The localized model name.</span></span><br/> <br/>                 |
| <span data-ttu-id="ccf22-115">**Lingua**</span><span class="sxs-lookup"><span data-stu-id="ccf22-115">**Language**</span></span><br/> | <span data-ttu-id="ccf22-116">stringa dell'identificatore di lingua</span><span class="sxs-lookup"><span data-stu-id="ccf22-116">language identifier string</span></span><br/>  | <span data-ttu-id="ccf22-117">Sì</span><span class="sxs-lookup"><span data-stu-id="ccf22-117">Yes</span></span><br/> | <span data-ttu-id="ccf22-118">Lingua del nome del modello localizzato.</span><span class="sxs-lookup"><span data-stu-id="ccf22-118">The language of the localized model name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="ccf22-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ccf22-119">Child elements</span></span>

<span data-ttu-id="ccf22-120">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="ccf22-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ccf22-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ccf22-121">Parent elements</span></span>



| <span data-ttu-id="ccf22-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="ccf22-122">Element</span></span>                                                   | <span data-ttu-id="ccf22-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccf22-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccf22-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="ccf22-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="ccf22-125">Definisce i metadati del produttore e del modello per il dispositivo da implementazione.</span><span class="sxs-lookup"><span data-stu-id="ccf22-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="ccf22-126">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ccf22-126">Element information</span></span>



| <span data-ttu-id="ccf22-127">Label</span><span class="sxs-lookup"><span data-stu-id="ccf22-127">Label</span></span> | <span data-ttu-id="ccf22-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf22-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ccf22-129">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf22-129">Minimum supported system</span></span><br/> | <span data-ttu-id="ccf22-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccf22-130">Windows Vista</span></span> |
| <span data-ttu-id="ccf22-131">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="ccf22-131">Can be empty</span></span>                        | <span data-ttu-id="ccf22-132">Sì</span><span class="sxs-lookup"><span data-stu-id="ccf22-132">Yes</span></span>           |



 

 





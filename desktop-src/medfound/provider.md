---
description: Specifica un provider di traccia (ETW o WPP) per MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118446"
---
# <a name="provider-element"></a><span data-ttu-id="ace07-103">provider (elemento)</span><span class="sxs-lookup"><span data-stu-id="ace07-103">provider element</span></span>

<span data-ttu-id="ace07-104">Specifica un provider di traccia (ETW o WPP) per [MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="ace07-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="ace07-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ace07-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="ace07-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="ace07-106">Attributes</span></span>



| <span data-ttu-id="ace07-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="ace07-107">Attribute</span></span>            | <span data-ttu-id="ace07-108">Type</span><span class="sxs-lookup"><span data-stu-id="ace07-108">Type</span></span>             | <span data-ttu-id="ace07-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="ace07-109">Required</span></span>       | <span data-ttu-id="ace07-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ace07-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="ace07-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="ace07-111">**ID**</span></span><br/>    | <span data-ttu-id="ace07-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="ace07-112">CDATA</span></span><br/> | <span data-ttu-id="ace07-113">Sì</span><span class="sxs-lookup"><span data-stu-id="ace07-113">Yes</span></span><br/> | <span data-ttu-id="ace07-114">Nome o GUID del provider.</span><span class="sxs-lookup"><span data-stu-id="ace07-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="ace07-115">**level**</span><span class="sxs-lookup"><span data-stu-id="ace07-115">**level**</span></span><br/> | <span data-ttu-id="ace07-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="ace07-116">CDATA</span></span><br/> | <span data-ttu-id="ace07-117">Sì</span><span class="sxs-lookup"><span data-stu-id="ace07-117">Yes</span></span><br/> | <span data-ttu-id="ace07-118">Livello di traccia.</span><span class="sxs-lookup"><span data-stu-id="ace07-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="ace07-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ace07-119">Child elements</span></span>



| <span data-ttu-id="ace07-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="ace07-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="ace07-121">**Parola chiave**</span><span class="sxs-lookup"><span data-stu-id="ace07-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="ace07-122">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ace07-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="ace07-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ace07-123">Parent elements</span></span>



| <span data-ttu-id="ace07-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="ace07-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="ace07-125">**Provider**</span><span class="sxs-lookup"><span data-stu-id="ace07-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="ace07-126">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ace07-126">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="ace07-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="ace07-127">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="ace07-128">No</span><span class="sxs-lookup"><span data-stu-id="ace07-128">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="ace07-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ace07-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace07-130">File di configurazione di MFTrace</span><span class="sxs-lookup"><span data-stu-id="ace07-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 





---
description: Specifica un provider di traccia (ETW o WPP) per MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753898"
---
# <a name="provider-element"></a><span data-ttu-id="d9599-103">provider (elemento)</span><span class="sxs-lookup"><span data-stu-id="d9599-103">provider element</span></span>

<span data-ttu-id="d9599-104">Specifica un provider di traccia (ETW o WPP) per [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="d9599-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d9599-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d9599-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="d9599-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="d9599-106">Attributes</span></span>



| <span data-ttu-id="d9599-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="d9599-107">Attribute</span></span>            | <span data-ttu-id="d9599-108">Type</span><span class="sxs-lookup"><span data-stu-id="d9599-108">Type</span></span>             | <span data-ttu-id="d9599-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d9599-109">Required</span></span>       | <span data-ttu-id="d9599-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9599-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="d9599-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="d9599-111">**ID**</span></span><br/>    | <span data-ttu-id="d9599-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="d9599-112">CDATA</span></span><br/> | <span data-ttu-id="d9599-113">Sì</span><span class="sxs-lookup"><span data-stu-id="d9599-113">Yes</span></span><br/> | <span data-ttu-id="d9599-114">Nome o GUID del provider.</span><span class="sxs-lookup"><span data-stu-id="d9599-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="d9599-115">**level**</span><span class="sxs-lookup"><span data-stu-id="d9599-115">**level**</span></span><br/> | <span data-ttu-id="d9599-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="d9599-116">CDATA</span></span><br/> | <span data-ttu-id="d9599-117">Sì</span><span class="sxs-lookup"><span data-stu-id="d9599-117">Yes</span></span><br/> | <span data-ttu-id="d9599-118">Livello di traccia.</span><span class="sxs-lookup"><span data-stu-id="d9599-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="d9599-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d9599-119">Child elements</span></span>



| <span data-ttu-id="d9599-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="d9599-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="d9599-121">**parola chiave**</span><span class="sxs-lookup"><span data-stu-id="d9599-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="d9599-122">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d9599-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="d9599-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d9599-123">Parent elements</span></span>



| <span data-ttu-id="d9599-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="d9599-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="d9599-125">**provider**</span><span class="sxs-lookup"><span data-stu-id="d9599-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="d9599-126">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d9599-126">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="d9599-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="d9599-127">Can be empty</span></span> | <span data-ttu-id="d9599-128">No</span><span class="sxs-lookup"><span data-stu-id="d9599-128">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="d9599-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d9599-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9599-130">File di configurazione MFTrace</span><span class="sxs-lookup"><span data-stu-id="d9599-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 





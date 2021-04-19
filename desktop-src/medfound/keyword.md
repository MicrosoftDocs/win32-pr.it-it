---
description: Specifica una parola chiave per un provider MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento Keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317309"
---
# <a name="keyword-element"></a><span data-ttu-id="6782a-103">elemento Keyword</span><span class="sxs-lookup"><span data-stu-id="6782a-103">keyword element</span></span>

<span data-ttu-id="6782a-104">Specifica una parola chiave per un provider [MFTrace](mftrace.md) .</span><span class="sxs-lookup"><span data-stu-id="6782a-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="6782a-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="6782a-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="6782a-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="6782a-106">Attributes</span></span>



| <span data-ttu-id="6782a-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="6782a-107">Attribute</span></span>         | <span data-ttu-id="6782a-108">Type</span><span class="sxs-lookup"><span data-stu-id="6782a-108">Type</span></span>             | <span data-ttu-id="6782a-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="6782a-109">Required</span></span>       | <span data-ttu-id="6782a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6782a-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="6782a-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="6782a-111">**ID**</span></span><br/> | <span data-ttu-id="6782a-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="6782a-112">CDATA</span></span><br/> | <span data-ttu-id="6782a-113">Sì</span><span class="sxs-lookup"><span data-stu-id="6782a-113">Yes</span></span><br/> | <span data-ttu-id="6782a-114">Nome o maschera della parola chiave</span><span class="sxs-lookup"><span data-stu-id="6782a-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="6782a-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6782a-115">Child elements</span></span>

<span data-ttu-id="6782a-116">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="6782a-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6782a-117">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="6782a-117">Parent elements</span></span>



| <span data-ttu-id="6782a-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="6782a-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="6782a-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="6782a-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="6782a-120">**provider**</span><span class="sxs-lookup"><span data-stu-id="6782a-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="6782a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6782a-121">Remarks</span></span>

<span data-ttu-id="6782a-122">Per l'elemento [**mfdetours**](mfdetours.md) , le parole chiave valide sono elencate nell'argomento [parole chiave MFTrace](mftrace-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="6782a-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="6782a-123">Per l'elemento [**provider**](provider.md) , le parole chiave dipendono dal provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="6782a-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="6782a-124">È possibile utilizzare l'utilità Wevtutil.exe per elencare le parole chiave per un determinato provider.</span><span class="sxs-lookup"><span data-stu-id="6782a-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="6782a-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6782a-125">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="6782a-126">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="6782a-126">Can be empty</span></span> | <span data-ttu-id="6782a-127">Sì</span><span class="sxs-lookup"><span data-stu-id="6782a-127">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="6782a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6782a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6782a-129">File di configurazione MFTrace</span><span class="sxs-lookup"><span data-stu-id="6782a-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="6782a-130">Parole chiave MFTrace</span><span class="sxs-lookup"><span data-stu-id="6782a-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 





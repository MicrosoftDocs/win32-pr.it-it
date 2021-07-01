---
description: Specifica una parola chiave per un provider MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba871fea760ed3b604048ade2722afc0323e03b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119376"
---
# <a name="keyword-element"></a><span data-ttu-id="03370-103">elemento keyword</span><span class="sxs-lookup"><span data-stu-id="03370-103">keyword element</span></span>

<span data-ttu-id="03370-104">Specifica una parola chiave per un provider [MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="03370-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="03370-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="03370-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="03370-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="03370-106">Attributes</span></span>



| <span data-ttu-id="03370-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="03370-107">Attribute</span></span>         | <span data-ttu-id="03370-108">Type</span><span class="sxs-lookup"><span data-stu-id="03370-108">Type</span></span>             | <span data-ttu-id="03370-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="03370-109">Required</span></span>       | <span data-ttu-id="03370-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03370-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="03370-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="03370-111">**ID**</span></span><br/> | <span data-ttu-id="03370-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="03370-112">CDATA</span></span><br/> | <span data-ttu-id="03370-113">Sì</span><span class="sxs-lookup"><span data-stu-id="03370-113">Yes</span></span><br/> | <span data-ttu-id="03370-114">Nome o maschera della parola chiave</span><span class="sxs-lookup"><span data-stu-id="03370-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="03370-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="03370-115">Child elements</span></span>

<span data-ttu-id="03370-116">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="03370-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="03370-117">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="03370-117">Parent elements</span></span>

| <span data-ttu-id="03370-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="03370-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="03370-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="03370-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="03370-120">**Provider**</span><span class="sxs-lookup"><span data-stu-id="03370-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="03370-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="03370-121">Remarks</span></span>

<span data-ttu-id="03370-122">Per [**l'elemento mfdetours,**](mfdetours.md) le parole chiave valide sono elencate nell'argomento [Parole chiave MFTrace](mftrace-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="03370-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="03370-123">Per [**l'elemento provider,**](provider.md) le parole chiave dipendono dal provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="03370-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="03370-124">È possibile usare l'Wevtutil.exe per elencare le parole chiave per un determinato provider.</span><span class="sxs-lookup"><span data-stu-id="03370-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="03370-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="03370-125">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="03370-126">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="03370-126">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="03370-127">Sì</span><span class="sxs-lookup"><span data-stu-id="03370-127">Yes</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="03370-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03370-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03370-129">File di configurazione di MFTrace</span><span class="sxs-lookup"><span data-stu-id="03370-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="03370-130">Parole chiave di MFTrace</span><span class="sxs-lookup"><span data-stu-id="03370-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 





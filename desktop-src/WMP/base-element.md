---
title: Elemento di BASE
description: L'elemento di BASE definisce una stringa URL aggiunta all'inizio degli URL inviati a Windows Media Player.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Windows elemento di BASE Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331018"
---
# <a name="base-element"></a><span data-ttu-id="8692f-104">Elemento di BASE</span><span class="sxs-lookup"><span data-stu-id="8692f-104">BASE Element</span></span>

<span data-ttu-id="8692f-105">L'elemento di **base** definisce una stringa URL aggiunta all'inizio degli URL inviati a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8692f-105">The **BASE** element defines a URL string appended to the front of URLs sent to Windows Media Player.</span></span>

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="8692f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="8692f-106">Attributes</span></span>

<span data-ttu-id="8692f-107">**Href** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="8692f-107">**HREF** (required)</span></span>

<span data-ttu-id="8692f-108">Stringa accodata all'inizio degli URL inviati a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8692f-108">The string appended to the front to URLs sent to Windows Media Player.</span></span> <span data-ttu-id="8692f-109">Il valore predefinito è la stringa null ("").</span><span class="sxs-lookup"><span data-stu-id="8692f-109">The default value is the null string ("").</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8692f-110">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="8692f-110">Parent/Child Elements</span></span>



| <span data-ttu-id="8692f-111">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="8692f-111">Hierarchy</span></span>       | <span data-ttu-id="8692f-112">Elementi</span><span class="sxs-lookup"><span data-stu-id="8692f-112">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="8692f-113">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8692f-113">Parent elements</span></span> | <span data-ttu-id="8692f-114">**ASX**, **voce**</span><span class="sxs-lookup"><span data-stu-id="8692f-114">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="8692f-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8692f-115">Child elements</span></span>  | <span data-ttu-id="8692f-116">nessuno</span><span class="sxs-lookup"><span data-stu-id="8692f-116">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="8692f-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8692f-117">Remarks</span></span>

<span data-ttu-id="8692f-118">Questo elemento definisce una stringa URL aggiunta all'inizio degli URL di capovolgimento URL inviati a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8692f-118">This element defines a URL string appended to the front of URL-flip URLs sent to Windows Media Player.</span></span> <span data-ttu-id="8692f-119">Il capovolgimento degli URL è un meccanismo di script che consente a Windows Media Player di aprire un nuovo URL in un browser o in un frame del browser quando riceve un comando per script.</span><span class="sxs-lookup"><span data-stu-id="8692f-119">URL-flipping is a scripting mechanism that causes Windows Media Player to open a new URL in a browser or browser frame when it receives a script command.</span></span>

<span data-ttu-id="8692f-120">L'elemento di **base** è simile a una home directory per i collegamenti relativi.</span><span class="sxs-lookup"><span data-stu-id="8692f-120">The **BASE** element is similar to a home directory for relative links.</span></span> <span data-ttu-id="8692f-121">Influiscono solo sugli URL inviati usando i comandi script come parte del flusso di contenuto che viene riprodotto in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8692f-121">It only affects URLs sent using script commands as part of the content stream that is playing in Windows Media Player.</span></span>

<span data-ttu-id="8692f-122">Un elemento di **base** definito come figlio di un elemento **ASX** diventa l'impostazione predefinita per l'intero metafile.</span><span class="sxs-lookup"><span data-stu-id="8692f-122">A **BASE** element defined as the child of an **ASX** element becomes the default for the entire metafile.</span></span> <span data-ttu-id="8692f-123">Un elemento di **base** definito in un elemento **entry** esegue l'override di qualsiasi elemento di **base** nell'elemento **ASX** padre (solo per tale elemento **entry** ).</span><span class="sxs-lookup"><span data-stu-id="8692f-123">A **BASE** element defined in an **ENTRY** element overrides any **BASE** element in the parent **ASX** element (for that **ENTRY** element only).</span></span>

> [!Note]  
> <span data-ttu-id="8692f-124">Se l'attributo **href** non termina con un carattere/, Windows Media Player ne aggiunge uno alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="8692f-124">If the **HREF** attribute does not end with a / character, Windows Media Player appends one to the end of the string.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8692f-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="8692f-125">Examples</span></span>


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a><span data-ttu-id="8692f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8692f-126">Requirements</span></span>



| <span data-ttu-id="8692f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8692f-127">Requirement</span></span> | <span data-ttu-id="8692f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8692f-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8692f-129">Versione</span><span class="sxs-lookup"><span data-stu-id="8692f-129">Version</span></span><br/> | <span data-ttu-id="8692f-130">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="8692f-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8692f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8692f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8692f-132">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8692f-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8692f-133">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8692f-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 






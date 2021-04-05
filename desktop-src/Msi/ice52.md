---
description: ICE52 verifica la presenza di proprietà private nella tabella AppSearch. Vedere informazioni sulle proprietà.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883934"
---
# <a name="ice52"></a><span data-ttu-id="99968-104">ICE52</span><span class="sxs-lookup"><span data-stu-id="99968-104">ICE52</span></span>

<span data-ttu-id="99968-105">ICE52 verifica la presenza di proprietà private nella [tabella AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="99968-105">ICE52 checks for private properties in the [AppSearch table](appsearch-table.md).</span></span> <span data-ttu-id="99968-106">Vedere [informazioni sulle proprietà](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="99968-106">See [About Properties](about-properties.md).</span></span>

<span data-ttu-id="99968-107">Quando si usa Windows 2000 tutte le proprietà impostate nella colonna proprietà della tabella AppSearch devono essere proprietà pubbliche.</span><span class="sxs-lookup"><span data-stu-id="99968-107">When using Windows 2000 all properties set in the Property column of the AppSearch table must be public properties.</span></span>

## <a name="result"></a><span data-ttu-id="99968-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="99968-108">Result</span></span>

<span data-ttu-id="99968-109">ICE52 pubblica un avviso se nella tabella AppSearch è presente una proprietà privata.</span><span class="sxs-lookup"><span data-stu-id="99968-109">ICE52 posts a warning if there is a private property in the AppSearch table.</span></span>

## <a name="example"></a><span data-ttu-id="99968-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="99968-110">Example</span></span>

<span data-ttu-id="99968-111">ICE52 invia l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="99968-111">ICE52 posts the following warning for the example shown.</span></span>

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[<span data-ttu-id="99968-112">Tabella AppSearch</span><span class="sxs-lookup"><span data-stu-id="99968-112">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="99968-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99968-113">Property</span></span>  | <span data-ttu-id="99968-114">Firma</span><span class="sxs-lookup"><span data-stu-id="99968-114">Signature</span></span>  |
|-----------|------------|
| <span data-ttu-id="99968-115">PROPERTY1</span><span class="sxs-lookup"><span data-stu-id="99968-115">PROPERTY1</span></span> | <span data-ttu-id="99968-116">Signature1</span><span class="sxs-lookup"><span data-stu-id="99968-116">Signature1</span></span> |
| <span data-ttu-id="99968-117">Property2</span><span class="sxs-lookup"><span data-stu-id="99968-117">Property2</span></span> | <span data-ttu-id="99968-118">Signature2</span><span class="sxs-lookup"><span data-stu-id="99968-118">Signature2</span></span> |



 

<span data-ttu-id="99968-119">Per correggere questa modifica di avviso nella proprietà pubblica personalizzata: PROPERTY2.</span><span class="sxs-lookup"><span data-stu-id="99968-119">To fix this warning change to the custom public property: PROPERTY2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99968-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99968-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99968-121">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="99968-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




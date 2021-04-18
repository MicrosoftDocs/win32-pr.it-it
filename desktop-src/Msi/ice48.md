---
description: ICE48 verifica la presenza di directory hardcoded in percorsi locali nella tabella delle proprietà.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314209"
---
# <a name="ice48"></a><span data-ttu-id="6881a-103">ICE48</span><span class="sxs-lookup"><span data-stu-id="6881a-103">ICE48</span></span>

<span data-ttu-id="6881a-104">ICE48 verifica la presenza di directory hardcoded in percorsi locali nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="6881a-104">ICE48 checks for directories that are hard-coded to local paths in the [Property table](property-table.md).</span></span>

<span data-ttu-id="6881a-105">Non impostare come hardcoded i percorsi della directory nelle unità locali perché i computer differiscono per la configurazione dell'unità locale.</span><span class="sxs-lookup"><span data-stu-id="6881a-105">Do not hard-code directory paths to local drives because computers differ in the setup of the local drive.</span></span> <span data-ttu-id="6881a-106">Questa pratica può essere accettabile se si distribuisce un'applicazione in un numero elevato di computer in cui le parti rilevanti delle unità sono tutte uguali.</span><span class="sxs-lookup"><span data-stu-id="6881a-106">This practice may be acceptable if deploying an application to a large number of computers on which the relevant portions of the drives are all the same.</span></span>

## <a name="result"></a><span data-ttu-id="6881a-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="6881a-107">Result</span></span>

<span data-ttu-id="6881a-108">ICE48 Invia un messaggio di errore se è presente una directory hardcoded in un percorso locale nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6881a-108">ICE48 posts an error message if there is a directory that is hard-coded to a local path in the Property table.</span></span>

## <a name="example"></a><span data-ttu-id="6881a-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="6881a-109">Example</span></span>

<span data-ttu-id="6881a-110">ICE48 segnala l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="6881a-110">ICE48 would report the following warning for the example shown.</span></span>

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

<span data-ttu-id="6881a-111">[Tabella directory](directory-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="6881a-111">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="6881a-112">Directory</span><span class="sxs-lookup"><span data-stu-id="6881a-112">Directory</span></span> | <span data-ttu-id="6881a-113">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="6881a-113">Directory\_Parent</span></span> | <span data-ttu-id="6881a-114">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="6881a-114">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="6881a-115">Dir1</span><span class="sxs-lookup"><span data-stu-id="6881a-115">Dir1</span></span>      |                   | <span data-ttu-id="6881a-116">SourceDir</span><span class="sxs-lookup"><span data-stu-id="6881a-116">SourceDir</span></span>  |



 

<span data-ttu-id="6881a-117">[Tabella delle proprietà](property-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="6881a-117">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="6881a-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6881a-118">Property</span></span> | <span data-ttu-id="6881a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6881a-119">Value</span></span>      |
|----------|------------|
| <span data-ttu-id="6881a-120">Dir1</span><span class="sxs-lookup"><span data-stu-id="6881a-120">Dir1</span></span>     | <span data-ttu-id="6881a-121">d: \\ origine</span><span class="sxs-lookup"><span data-stu-id="6881a-121">d:\\source</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6881a-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6881a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6881a-123">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="6881a-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




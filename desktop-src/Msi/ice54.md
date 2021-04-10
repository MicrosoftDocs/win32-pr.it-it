---
description: ICE54 verifica la presenza di componenti che usano un file complementare come percorso della chiave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882121"
---
# <a name="ice54"></a><span data-ttu-id="e66fa-103">ICE54</span><span class="sxs-lookup"><span data-stu-id="e66fa-103">ICE54</span></span>

<span data-ttu-id="e66fa-104">ICE54 verifica la presenza di componenti che usano un file complementare come percorso della chiave.</span><span class="sxs-lookup"><span data-stu-id="e66fa-104">ICE54 checks for components that use a companion file as their key path.</span></span>

<span data-ttu-id="e66fa-105">Il file del percorso della chiave di un componente non deve derivare la propria versione da un file diverso.</span><span class="sxs-lookup"><span data-stu-id="e66fa-105">The key path file of a component must not derive its version from a different file.</span></span> <span data-ttu-id="e66fa-106">Questo può causare un errore di installazione di alcuni file.</span><span class="sxs-lookup"><span data-stu-id="e66fa-106">This can cause some files to fail to install.</span></span> <span data-ttu-id="e66fa-107">Per ulteriori informazioni sui file complementari, vedere la [tabella dei file](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e66fa-107">See the [File table](file-table.md) for more information about companion files.</span></span>

## <a name="result"></a><span data-ttu-id="e66fa-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="e66fa-108">Result</span></span>

<span data-ttu-id="e66fa-109">ICE54 pubblica un avviso se un componente dispone di un file di percorso della chiave che deriva la versione da un altro file.</span><span class="sxs-lookup"><span data-stu-id="e66fa-109">ICE54 posts a warning if any component has a key path file that derives its version from another file.</span></span>

## <a name="example"></a><span data-ttu-id="e66fa-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="e66fa-110">Example</span></span>

<span data-ttu-id="e66fa-111">ICE54 restituisce l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="e66fa-111">ICE54 returns the following warning for the example shown.</span></span>

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

<span data-ttu-id="e66fa-112">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e66fa-112">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="e66fa-113">Componente</span><span class="sxs-lookup"><span data-stu-id="e66fa-113">Component</span></span>  | <span data-ttu-id="e66fa-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="e66fa-114">Attribute</span></span> | <span data-ttu-id="e66fa-115">KeyPath</span><span class="sxs-lookup"><span data-stu-id="e66fa-115">KeyPath</span></span> |
|------------|-----------|---------|
| <span data-ttu-id="e66fa-116">Component1</span><span class="sxs-lookup"><span data-stu-id="e66fa-116">Component1</span></span> | <span data-ttu-id="e66fa-117">0</span><span class="sxs-lookup"><span data-stu-id="e66fa-117">0</span></span>         | <span data-ttu-id="e66fa-118">File1</span><span class="sxs-lookup"><span data-stu-id="e66fa-118">File1</span></span>   |



 

<span data-ttu-id="e66fa-119">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e66fa-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="e66fa-120">File</span><span class="sxs-lookup"><span data-stu-id="e66fa-120">File</span></span>  | <span data-ttu-id="e66fa-121">Versione</span><span class="sxs-lookup"><span data-stu-id="e66fa-121">Version</span></span> | <span data-ttu-id="e66fa-122">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="e66fa-122">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="e66fa-123">File1</span><span class="sxs-lookup"><span data-stu-id="e66fa-123">File1</span></span> | <span data-ttu-id="e66fa-124">File2</span><span class="sxs-lookup"><span data-stu-id="e66fa-124">File2</span></span>   |          |
| <span data-ttu-id="e66fa-125">File2</span><span class="sxs-lookup"><span data-stu-id="e66fa-125">File2</span></span> | <span data-ttu-id="e66fa-126">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="e66fa-126">1.0.0.0</span></span> | <span data-ttu-id="e66fa-127">1033</span><span class="sxs-lookup"><span data-stu-id="e66fa-127">1033</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="e66fa-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e66fa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e66fa-129">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e66fa-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




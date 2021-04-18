---
description: ICE56 verifica che la struttura di directory del file con estensione msi disponga di una singola directory radice, che la radice sia la proprietà TARGETDIR e che il valore della proprietà SourceDir sia presente nella colonna DefaultDir della tabella di directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315904"
---
# <a name="ice56"></a><span data-ttu-id="80163-103">ICE56</span><span class="sxs-lookup"><span data-stu-id="80163-103">ICE56</span></span>

<span data-ttu-id="80163-104">ICE56 verifica che la struttura di directory del file con estensione msi disponga di una singola directory radice, che la radice sia la proprietà [**targetdir**](targetdir.md) e che il valore della proprietà [**SourceDir**](sourcedir.md) sia presente nella colonna DefaultDir della [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="80163-104">ICE56 validates that the directory structure of the .msi file has a single root directory, that the root is the [**TARGETDIR**](targetdir.md) property, and that the [**SourceDir**](sourcedir.md) property value is in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="80163-105">Se un file con estensione MSI ha più radici o specifica una radice diversa da [**targetdir**](targetdir.md), un' [installazione amministrativa](administrative-installation.md) non crea un'immagine amministrativa corretta.</span><span class="sxs-lookup"><span data-stu-id="80163-105">If a .msi file has multiple roots or specifies a root other than [**TARGETDIR**](targetdir.md), an [administrative installation](administrative-installation.md) does not create a correct administrative image.</span></span>

<span data-ttu-id="80163-106">Si noti che le directory vuote non vengono controllate da ICE56.</span><span class="sxs-lookup"><span data-stu-id="80163-106">Note that empty directories are not checked by ICE56.</span></span> <span data-ttu-id="80163-107">La struttura di directory passa la convalida a più directory radice se le directory aggiuntive sono vuote.</span><span class="sxs-lookup"><span data-stu-id="80163-107">The directory structure passes validation with multiple root directories if the extra directories are empty.</span></span>

## <a name="result"></a><span data-ttu-id="80163-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="80163-108">Result</span></span>

<span data-ttu-id="80163-109">ICE56 Invia un errore se il file con estensione msi non dispone di una sola radice, [**targetdir**](targetdir.md)o se [**SourceDir**](sourcedir.md) non è specificato nella colonna DefaultDir della [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="80163-109">ICE56 posts an error if the .msi does not have a single root, [**TARGETDIR**](targetdir.md), or if [**SourceDir**](sourcedir.md) is not specified in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="80163-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="80163-110">Example</span></span>

<span data-ttu-id="80163-111">ICE56 segnala gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="80163-111">ICE56 reports the following errors for the example shown.</span></span>

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[<span data-ttu-id="80163-112">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="80163-112">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="80163-113">Directory</span><span class="sxs-lookup"><span data-stu-id="80163-113">Directory</span></span> | <span data-ttu-id="80163-114">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="80163-114">Directory\_Parent</span></span> | <span data-ttu-id="80163-115">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="80163-115">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="80163-116">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="80163-116">TARGETDIR</span></span> |                   | <span data-ttu-id="80163-117">Temp</span><span class="sxs-lookup"><span data-stu-id="80163-117">Temp</span></span>       |
| <span data-ttu-id="80163-118">ROOT2</span><span class="sxs-lookup"><span data-stu-id="80163-118">Root2</span></span>     | <span data-ttu-id="80163-119">ROOT2</span><span class="sxs-lookup"><span data-stu-id="80163-119">Root2</span></span>             | <span data-ttu-id="80163-120">SourceDir</span><span class="sxs-lookup"><span data-stu-id="80163-120">SourceDir</span></span>  |



 

<span data-ttu-id="80163-121">Per correggere il primo errore, la radice [**targetdir**](targetdir.md) deve avere il valore DefaultDir [**SourceDir**](sourcedir.md).</span><span class="sxs-lookup"><span data-stu-id="80163-121">To fix the first error, the [**TARGETDIR**](targetdir.md) root should have a DefaultDir value of [**SourceDir**](sourcedir.md).</span></span> <span data-ttu-id="80163-122">Viene inoltre accettata SOURCEDIR.</span><span class="sxs-lookup"><span data-stu-id="80163-122">SOURCEDIR is also accepted.</span></span> <span data-ttu-id="80163-123">Potrebbe essere possibile rendere **targetdir** il padre della seconda radice e usare il valore ' .' nella colonna DefaultDir.</span><span class="sxs-lookup"><span data-stu-id="80163-123">It may be possible to make **TARGETDIR** the parent of the second root, and use the '.' value in the DefaultDir column.</span></span> <span data-ttu-id="80163-124">Per ulteriori informazioni, vedere la [tabella directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="80163-124">See the [Directory table](directory-table.md) for more information.</span></span>

<span data-ttu-id="80163-125">Per correggere il secondo errore, la struttura di directory deve avere solo una radice denominata [**targetdir**](targetdir.md).</span><span class="sxs-lookup"><span data-stu-id="80163-125">To fix the second error, the Directory structure should have only one root called [**TARGETDIR**](targetdir.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80163-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80163-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80163-127">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="80163-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




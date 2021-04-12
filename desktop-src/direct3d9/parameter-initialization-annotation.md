---
description: Usare questa annotazione per definire il contenuto di un file esterno come valore di inizializzazione per un parametro di effetto.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Annotazione inizializzazione parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225334"
---
# <a name="parameter-initialization-annotation"></a><span data-ttu-id="73ee4-103">Annotazione inizializzazione parametri</span><span class="sxs-lookup"><span data-stu-id="73ee4-103">Parameter Initialization Annotation</span></span>

<span data-ttu-id="73ee4-104">Usare questa annotazione per definire il contenuto di un file esterno come valore di inizializzazione per un parametro di effetto.</span><span class="sxs-lookup"><span data-stu-id="73ee4-104">Use this annotation to define the contents of an external file as the initialization value for an effect parameter.</span></span> <span data-ttu-id="73ee4-105">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="73ee4-105">For example:</span></span>


```
string SasResourceAddress = "Value";
```



<span data-ttu-id="73ee4-106">dove value è una stringa di testo ASCII che può contenere un percorso assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="73ee4-106">where Value is an ASCII text string that may contain an absolute or relative path.</span></span> <span data-ttu-id="73ee4-107">Un percorso relativo è relativo alla directory che contiene il file di effetti.</span><span class="sxs-lookup"><span data-stu-id="73ee4-107">A relative path is relative to the directory that contains the effect file.</span></span>

<span data-ttu-id="73ee4-108">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="73ee4-108">Here is an example:</span></span>


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



<span data-ttu-id="73ee4-109">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="73ee4-109">The default value is an empty string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73ee4-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73ee4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73ee4-111">Informazioni di riferimento sulla semantica e le annotazioni standard DirectX</span><span class="sxs-lookup"><span data-stu-id="73ee4-111">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 




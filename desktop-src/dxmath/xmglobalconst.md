---
description: Dichiara un oggetto come una costante pick-any, per evitare ricaricamenti ridondanti di tale oggetto se viene usato (e dichiarato) in più posizioni nella libreria DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST (macro)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309220"
---
# <a name="xmglobalconst-macro"></a><span data-ttu-id="476d1-103">XMGLOBALCONST (macro)</span><span class="sxs-lookup"><span data-stu-id="476d1-103">XMGLOBALCONST macro</span></span>

<span data-ttu-id="476d1-104">Dichiara un oggetto come una costante *pick-any* , per evitare ricaricamenti ridondanti di tale oggetto se viene usato (e dichiarato) in più posizioni nella libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="476d1-104">Declares an object to be a *pick-any* constant, to avoid redundant reloads of that object if it is used (and declared) in multiple places in the DirectXMath Library.</span></span>

## <a name="syntax"></a><span data-ttu-id="476d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="476d1-105">Syntax</span></span>

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a><span data-ttu-id="476d1-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="476d1-106">Remarks</span></span>

<span data-ttu-id="476d1-107">L'uso di XMGLOBALCONST consente di specificare le costanti globali.</span><span class="sxs-lookup"><span data-stu-id="476d1-107">Using XMGLOBALCONST permits the specification of global constants.</span></span> <span data-ttu-id="476d1-108">Ciò consente di ridurre le dimensioni del segmento di dati di un'applicazione, evitare la creazione e l'eliminazione di oggetti ridondanti e ridurre le operazioni di caricamento e archiviazione.</span><span class="sxs-lookup"><span data-stu-id="476d1-108">This helps to reduce the size of an application's data segment, avoid redundant object creation and destruction, and reduce load and store operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="476d1-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="476d1-109">Requirements</span></span>

<span data-ttu-id="476d1-110">**Intestazione:** Dichiarata in DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="476d1-110">**Header:** Declared in DirectXMath.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="476d1-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="476d1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="476d1-112">Macro della libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="476d1-112">DirectXMath Library Macros</span></span>](ovw-xnamath-reference-macros.md)
</dt> <dt>

[<span data-ttu-id="476d1-113">Costanti globali nella libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="476d1-113">Global Constants in the DirectXMath Library</span></span>](pg-xnamath-internals.md)
</dt> <dt>

<span data-ttu-id="476d1-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="476d1-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span></span>
</dt> <dt>

<span data-ttu-id="476d1-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="476d1-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span></span>
</dt> </dl>

 

 

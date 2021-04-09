---
description: Rappresenta una descrizione di una sezione di trama.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixEngineTextureSliceDescriptor
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123981"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span data-ttu-id="14995-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>Struttura PixEngineTextureSliceDescriptor</span><span class="sxs-lookup"><span data-stu-id="14995-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor structure</span></span>

<span data-ttu-id="14995-104">Rappresenta una descrizione di una sezione di trama.</span><span class="sxs-lookup"><span data-stu-id="14995-104">Represents a description of a texture slice.</span></span>

## <a name="syntax"></a><span data-ttu-id="14995-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14995-105">Syntax</span></span>


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a><span data-ttu-id="14995-106">Members</span><span class="sxs-lookup"><span data-stu-id="14995-106">Members</span></span>

<span data-ttu-id="14995-107">**width**</span><span class="sxs-lookup"><span data-stu-id="14995-107">**width**</span></span>  
<span data-ttu-id="14995-108">Larghezza (numero di campioni nell'asse X) della sezione.</span><span class="sxs-lookup"><span data-stu-id="14995-108">The width (number of samples in the X axis) of the slice.</span></span>

<span data-ttu-id="14995-109">**height**</span><span class="sxs-lookup"><span data-stu-id="14995-109">**height**</span></span>  
<span data-ttu-id="14995-110">Altezza (numero di campioni nell'asse Y) della sezione.</span><span class="sxs-lookup"><span data-stu-id="14995-110">The height (number of samples in the Y axis) of the slice.</span></span>

<span data-ttu-id="14995-111">**blockRowBytes**</span><span class="sxs-lookup"><span data-stu-id="14995-111">**blockRowBytes**</span></span>  
<span data-ttu-id="14995-112">Numero di byte per riga in ogni blocco.</span><span class="sxs-lookup"><span data-stu-id="14995-112">The number of bytes per row in each block.</span></span>

<span data-ttu-id="14995-113">**offset**</span><span class="sxs-lookup"><span data-stu-id="14995-113">**offset**</span></span>  
<span data-ttu-id="14995-114">Offset della sezione all'interno dell'intera trama.</span><span class="sxs-lookup"><span data-stu-id="14995-114">The offset of the slice within the whole texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="14995-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14995-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="14995-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14995-116">Header</span></span></p></td><td><span data-ttu-id="14995-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="14995-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




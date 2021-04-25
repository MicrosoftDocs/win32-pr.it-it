---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Rappresenta i dati bitmap in formato BGRA32.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: ad36eb8fe691330b471db0b7e8b5378f3e7614db
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955054"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="a59db-103">DWRITE_BITMAP_DATA_BGRA32 struttura (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="a59db-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="a59db-104">Rappresenta i dati bitmap in formato BGRA32.</span><span class="sxs-lookup"><span data-stu-id="a59db-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a59db-105">Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="a59db-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="a59db-106">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="a59db-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="a59db-107">Per altre informazioni ed esempi di codice, vedere [Panoramica di DWriteCore.](/windows/win32/directwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="a59db-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="a59db-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a59db-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="a59db-109">Members</span><span class="sxs-lookup"><span data-stu-id="a59db-109">Members</span></span>

`width`

<span data-ttu-id="a59db-110">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a59db-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a59db-111">Larghezza, in pixel, della bitmap.</span><span class="sxs-lookup"><span data-stu-id="a59db-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="a59db-112">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a59db-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a59db-113">Altezza, in pixel, della bitmap.</span><span class="sxs-lookup"><span data-stu-id="a59db-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="a59db-114">Tipo: \_ Dimensioni \_ campo \_ (larghezza \* altezza)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a59db-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a59db-115">Puntatore alla posizione dei valori di bit per la bitmap.</span><span class="sxs-lookup"><span data-stu-id="a59db-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="a59db-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="a59db-116">Examples</span></span>

<span data-ttu-id="a59db-117">Vedere [l'argomento di panoramica di DWriteCore](/windows/win32/directwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="a59db-117">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="a59db-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a59db-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a59db-119">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="a59db-119">**Minimum supported client**</span></span> | <span data-ttu-id="a59db-120">Windows 10, Project Reunion [app Win32]</span><span class="sxs-lookup"><span data-stu-id="a59db-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="a59db-121">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="a59db-121">**Header**</span></span> | <span data-ttu-id="a59db-122">dwrite_3.h (includere dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="a59db-122">dwrite_3.h (include dwrite_core.h)</span></span> |
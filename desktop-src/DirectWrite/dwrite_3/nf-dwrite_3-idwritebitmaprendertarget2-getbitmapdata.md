---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Recupera i dati pixel da una destinazione di rendering bitmap.
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: f84959338550722d9ce1d2d7097d652fcb140f1f
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955044"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="fb5dc-103">Metodo IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="fb5dc-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="fb5dc-104">Recupera i dati pixel da una destinazione di rendering bitmap.</span><span class="sxs-lookup"><span data-stu-id="fb5dc-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb5dc-105">Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="fb5dc-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="fb5dc-106">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="fb5dc-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="fb5dc-107">Per altre informazioni ed esempi di codice, vedere [Panoramica di DWriteCore.](/windows/win32/directwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="fb5dc-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb5dc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb5dc-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="fb5dc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb5dc-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="fb5dc-110">Tipo: \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb5dc-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="fb5dc-111">Puntatore ai dati pixel.</span><span class="sxs-lookup"><span data-stu-id="fb5dc-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb5dc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb5dc-112">Return value</span></span>

<span data-ttu-id="fb5dc-113">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="fb5dc-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="fb5dc-114">Se questo metodo ha esito positivo, <b xmlns:loc="http://microsoft.com/wdcml/l10n">restituisce</b>S_OK .</span><span class="sxs-lookup"><span data-stu-id="fb5dc-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="fb5dc-115">In caso contrario, restituisce un <b xmlns:loc="http://microsoft.com/wdcml/l10n">codice di errore HRESULT.</b></span><span class="sxs-lookup"><span data-stu-id="fb5dc-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="fb5dc-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="fb5dc-116">Examples</span></span>

<span data-ttu-id="fb5dc-117">Vedere [l'argomento di panoramica di DWriteCore](/windows/win32/directwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="fb5dc-117">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb5dc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb5dc-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fb5dc-119">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="fb5dc-119">**Minimum supported client**</span></span> | <span data-ttu-id="fb5dc-120">Windows 10, Project Reunion [app Win32]</span><span class="sxs-lookup"><span data-stu-id="fb5dc-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="fb5dc-121">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="fb5dc-121">**Header**</span></span> | <span data-ttu-id="fb5dc-122">dwrite_3.h (includere dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="fb5dc-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="fb5dc-123">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="fb5dc-123">**Library**</span></span> | <span data-ttu-id="fb5dc-124">Dwrite.lib</span><span class="sxs-lookup"><span data-stu-id="fb5dc-124">Dwrite.lib</span></span> |
| <span data-ttu-id="fb5dc-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="fb5dc-125">**DLL**</span></span> | <span data-ttu-id="fb5dc-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="fb5dc-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="fb5dc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb5dc-127">See also</span></span>

[<span data-ttu-id="fb5dc-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="fb5dc-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)

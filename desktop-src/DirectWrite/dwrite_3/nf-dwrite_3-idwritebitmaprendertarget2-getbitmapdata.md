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
ms.openlocfilehash: 15a51fdea0d7e579e427ab52af3016e58a39831a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550286"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="a1d06-103">Metodo IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="a1d06-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="a1d06-104">Recupera i dati pixel da una destinazione di rendering bitmap.</span><span class="sxs-lookup"><span data-stu-id="a1d06-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1d06-105">Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="a1d06-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="a1d06-106">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="a1d06-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="a1d06-107">Per altre informazioni ed esempi di codice, vedi [Panoramica di DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a1d06-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d06-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1d06-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="a1d06-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1d06-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="a1d06-110">Tipo: \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1d06-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="a1d06-111">Puntatore ai dati pixel.</span><span class="sxs-lookup"><span data-stu-id="a1d06-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1d06-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1d06-112">Return value</span></span>

<span data-ttu-id="a1d06-113">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="a1d06-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="a1d06-114">Se questo metodo ha esito positivo, restituisce <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="a1d06-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="a1d06-115">In caso contrario, restituisce un <b xmlns:loc="http://microsoft.com/wdcml/l10n">codice di errore HRESULT.</b></span><span class="sxs-lookup"><span data-stu-id="a1d06-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="a1d06-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="a1d06-116">Examples</span></span>

<span data-ttu-id="a1d06-117">Vedere [l'argomento di panoramica DWriteCore](../dwritecore-overview.md) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="a1d06-117">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d06-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1d06-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a1d06-119">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="a1d06-119">**Minimum supported client**</span></span> | <span data-ttu-id="a1d06-120">Windows 10, Project Dispositivi [app Win32]</span><span class="sxs-lookup"><span data-stu-id="a1d06-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="a1d06-121">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="a1d06-121">**Header**</span></span> | <span data-ttu-id="a1d06-122">dwrite_3.h (includere dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="a1d06-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="a1d06-123">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="a1d06-123">**Library**</span></span> | <span data-ttu-id="a1d06-124">Dwrite.lib</span><span class="sxs-lookup"><span data-stu-id="a1d06-124">Dwrite.lib</span></span> |
| <span data-ttu-id="a1d06-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="a1d06-125">**DLL**</span></span> | <span data-ttu-id="a1d06-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="a1d06-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="a1d06-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1d06-127">See also</span></span>

[<span data-ttu-id="a1d06-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="a1d06-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)
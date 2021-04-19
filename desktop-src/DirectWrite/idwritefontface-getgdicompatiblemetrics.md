---
title: Metodo IDWriteFontFace GetGdiCompatibleMetrics
description: Ottiene le unità di progettazione e le metriche comuni per il tipo di carattere. Queste metriche sono applicabili a tutti i glifi all'interno di una fontFace e vengono usate dalle applicazioni per i calcoli di layout.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Scrittura diretta metodo GetGdiCompatibleMetrics
- Metodo GetGdiCompatibleMetrics scrittura diretta, interfaccia IDWriteFontFace
- IDWriteFontFace interface Direct Write, metodo GetGdiCompatibleMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325904"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a><span data-ttu-id="e5e4e-107">Metodo IDWriteFontFace:: GetGdiCompatibleMetrics</span><span class="sxs-lookup"><span data-stu-id="e5e4e-107">IDWriteFontFace::GetGdiCompatibleMetrics method</span></span>

<span data-ttu-id="e5e4e-108">Ottiene le unità di progettazione e le metriche comuni per il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-108">Obtains design units and common metrics for the font face.</span></span> <span data-ttu-id="e5e4e-109">Queste metriche sono applicabili a tutti i glifi all'interno di una fontFace e vengono usate dalle applicazioni per i calcoli di layout.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-109">These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e4e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5e4e-110">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e5e4e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5e4e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e4e-112">*emSize*</span><span class="sxs-lookup"><span data-stu-id="e5e4e-112">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="e5e4e-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e5e4e-113">Type: **FLOAT**</span></span>

<span data-ttu-id="e5e4e-114">Dimensioni logiche del tipo di carattere in unità DIP.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-114">The logical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="e5e4e-115">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="e5e4e-115">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="e5e4e-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e5e4e-116">Type: **FLOAT**</span></span>

<span data-ttu-id="e5e4e-117">Il numero di pixel fisici per DIP.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-117">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="e5e4e-118">*trasformazione* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5e4e-118">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e4e-119">Tipo: **const [**DWrite \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="e5e4e-119">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="e5e4e-120">Trasformazione facoltativa applicata ai glifi e alle rispettive posizioni.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-120">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="e5e4e-121">Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e da *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-121">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="e5e4e-122">*fontFaceMetrics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e5e4e-122">*fontFaceMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e4e-123">Tipo: metrica del tipo di **[ **\_ carattere \_ DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="e5e4e-123">Type: **[**DWRITE\_FONT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span></span>

<span data-ttu-id="e5e4e-124">Puntatore a una struttura [**della \_ \_ metrica del tipo di carattere DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)da compilare.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-124">A pointer to a [**DWRITE\_FONT\_METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S structure to fill in.</span></span> <span data-ttu-id="e5e4e-125">Le metriche restituite da questa funzione sono in unità di progettazione dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-125">The metrics returned by this function are in font design units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5e4e-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5e4e-126">Return value</span></span>

<span data-ttu-id="e5e4e-127">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e5e4e-127">Type: **HRESULT**</span></span>

<span data-ttu-id="e5e4e-128">Codice di errore HRESULT standard.</span><span class="sxs-lookup"><span data-stu-id="e5e4e-128">Standard HRESULT error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e4e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5e4e-129">Requirements</span></span>



| <span data-ttu-id="e5e4e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5e4e-130">Requirement</span></span> | <span data-ttu-id="e5e4e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e5e4e-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e4e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5e4e-132">Library</span></span><br/> | <dl> <span data-ttu-id="e5e4e-133"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5e4e-133"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5e4e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e5e4e-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5e4e-135"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5e4e-135"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5e4e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5e4e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e4e-137">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="e5e4e-137">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="e5e4e-138">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="e5e4e-138">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 


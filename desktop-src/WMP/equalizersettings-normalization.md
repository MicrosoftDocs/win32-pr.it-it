---
title: EQUALIZERSETTINGS. normalizzazione
description: L'attributo di normalizzazione specifica o recupera un valore che indica se la normalizzazione è abilitata.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normalizzazione di Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326127"
---
# <a name="equalizersettingsnormalization"></a><span data-ttu-id="a8a5e-104">EQUALIZERSETTINGS. normalizzazione</span><span class="sxs-lookup"><span data-stu-id="a8a5e-104">EQUALIZERSETTINGS.normalization</span></span>

<span data-ttu-id="a8a5e-105">L'attributo di **normalizzazione** specifica o recupera un valore che indica se la normalizzazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-105">The **normalization** attribute specifies or retrieves a value indicating whether normalization is enabled.</span></span>

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a><span data-ttu-id="a8a5e-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a8a5e-106">Possible Values</span></span>

<span data-ttu-id="a8a5e-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a8a5e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a8a5e-108">Value</span></span> | <span data-ttu-id="a8a5e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8a5e-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="a8a5e-110">true</span><span class="sxs-lookup"><span data-stu-id="a8a5e-110">true</span></span>  | <span data-ttu-id="a8a5e-111">La normalizzazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-111">Normalization is enabled.</span></span>           |
| <span data-ttu-id="a8a5e-112">false</span><span class="sxs-lookup"><span data-stu-id="a8a5e-112">false</span></span> | <span data-ttu-id="a8a5e-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-113">Default.</span></span> <span data-ttu-id="a8a5e-114">La normalizzazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-114">Normalization is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a8a5e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8a5e-115">Remarks</span></span>

<span data-ttu-id="a8a5e-116">Quando è abilitata la normalizzazione, il segnale audio per un intero file multimediale digitale viene scalato fino al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-116">When normalization is enabled, the audio signal for an entire digital media file is scaled up to the maximum value.</span></span> <span data-ttu-id="a8a5e-117">In questo modo è possibile riprodurre più file approssimativamente nello stesso volume senza che sia necessario apportare modifiche al volume.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-117">This allows multiple files to be played at approximately the same volume without requiring volume adjustments.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a5e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8a5e-118">Requirements</span></span>



| <span data-ttu-id="a8a5e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8a5e-119">Requirement</span></span> | <span data-ttu-id="a8a5e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a8a5e-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a8a5e-121">Versione</span><span class="sxs-lookup"><span data-stu-id="a8a5e-121">Version</span></span><br/> | <span data-ttu-id="a8a5e-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a8a5e-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8a5e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8a5e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a5e-124">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="a8a5e-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="a8a5e-125">**EQUALIZERSETTINGS.normalizationAverage**</span><span class="sxs-lookup"><span data-stu-id="a8a5e-125">**EQUALIZERSETTINGS.normalizationAverage**</span></span>](equalizersettings-normalizationaverage.md)
</dt> <dt>

[<span data-ttu-id="a8a5e-126">**EQUALIZERSETTINGS.normalizationPeak**</span><span class="sxs-lookup"><span data-stu-id="a8a5e-126">**EQUALIZERSETTINGS.normalizationPeak**</span></span>](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 






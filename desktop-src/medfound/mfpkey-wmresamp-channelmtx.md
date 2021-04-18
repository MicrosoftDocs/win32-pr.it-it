---
description: Specifica la matrice del canale utilizzata per convertire i canali di origine nei canali di destinazione (ad esempio, per convertire 5,1 in stereo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: Proprietà MFPKEY_WMRESAMP_CHANNELMTX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310258"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a><span data-ttu-id="09ebc-103">MFPKEY \_ WMRESAMP- \_ Proprietà CHANNELMTX</span><span class="sxs-lookup"><span data-stu-id="09ebc-103">MFPKEY\_WMRESAMP\_CHANNELMTX Property</span></span>

<span data-ttu-id="09ebc-104">Specifica la matrice del canale utilizzata per convertire i canali di origine nei canali di destinazione (ad esempio, per convertire 5,1 in stereo).</span><span class="sxs-lookup"><span data-stu-id="09ebc-104">Specifies the channel matrix, which is used to convert the source channels into the destination channels (for example, to convert 5.1 to stereo).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="09ebc-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="09ebc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="09ebc-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="09ebc-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="09ebc-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="09ebc-107">Data Type</span></span>

<span data-ttu-id="09ebc-108">\_Array VT I4 VT \| \_</span><span class="sxs-lookup"><span data-stu-id="09ebc-108">VT\_I4 \| VT\_ARRAY</span></span>

## <a name="applies-to"></a><span data-ttu-id="09ebc-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="09ebc-109">Applies To</span></span>

-   [<span data-ttu-id="09ebc-110">DSP ricampionatore audio</span><span class="sxs-lookup"><span data-stu-id="09ebc-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="09ebc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="09ebc-111">Remarks</span></span>

<span data-ttu-id="09ebc-112">Il valore della proprietà è una matrice di coefficienti NS x ND, dove NS è il numero di canali di origine e ND è il numero di canali di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09ebc-112">The value of the property is a matrix of Ns x Nd coefficients, where Ns is the number of source channels and Nd is the number of destination channels.</span></span> <span data-ttu-id="09ebc-113">I coefficienti vengono specificati in decibel usando la formula seguente:</span><span class="sxs-lookup"><span data-stu-id="09ebc-113">Coefficients are specified in decibels using the following formula:</span></span>

<span data-ttu-id="09ebc-114">int (65536 \* 20 \* log10 (DB))</span><span class="sxs-lookup"><span data-stu-id="09ebc-114">(int)(65536\*20\*log10(dB))</span></span>

<span data-ttu-id="09ebc-115">La matrice viene archiviata come matrice nell'ordine principale della riga in cui il numero di riga è il canale di origine e il numero di colonna è il canale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09ebc-115">The matrix is stored as an array in row-major order where the row number is the source channel and the column number is the destination channel.</span></span>

<span data-ttu-id="09ebc-116">Quindi, se la matrice è la seguente:</span><span class="sxs-lookup"><span data-stu-id="09ebc-116">Thus, if the matrix is the following:</span></span>

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

<span data-ttu-id="09ebc-117">Specificare quindi la matrice come:</span><span class="sxs-lookup"><span data-stu-id="09ebc-117">then you would specify the array as:</span></span>

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a><span data-ttu-id="09ebc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09ebc-118">Requirements</span></span>



| <span data-ttu-id="09ebc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="09ebc-119">Requirement</span></span> | <span data-ttu-id="09ebc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="09ebc-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09ebc-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09ebc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="09ebc-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="09ebc-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="09ebc-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09ebc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="09ebc-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09ebc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="09ebc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09ebc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ebc-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="09ebc-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ebc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09ebc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ebc-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09ebc-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

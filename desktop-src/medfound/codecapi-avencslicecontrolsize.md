---
description: Specifica le dimensioni della sezione in unità di megabyte (MB), bits o MB di riga.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Proprietà CODECAPI_AVEncSliceControlSize (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127978"
---
# <a name="codecapi_avencslicecontrolsize-property"></a><span data-ttu-id="5f9e4-103">Proprietà AVEncSliceControlSize di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="5f9e4-103">CODECAPI\_AVEncSliceControlSize property</span></span>

<span data-ttu-id="5f9e4-104">Specifica le dimensioni della sezione in unità di megabyte (MB), bits o MB di riga.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-104">Specifies the size of the slice in units of megabyte (MB), bits, or MB row.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f9e4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5f9e4-105">Data type</span></span>

<span data-ttu-id="5f9e4-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="5f9e4-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5f9e4-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="5f9e4-107">Property GUID</span></span>

<span data-ttu-id="5f9e4-108">**Codecapis \_ AVEncSliceControlSize**</span><span class="sxs-lookup"><span data-stu-id="5f9e4-108">**CODECAPI\_AVEncSliceControlSize**</span></span>

## <a name="remarks"></a><span data-ttu-id="5f9e4-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f9e4-109">Remarks</span></span>

<span data-ttu-id="5f9e4-110">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="5f9e4-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="5f9e4-111">Il significato del valore di codecapis \_ AVEncSliceControlSize è controllato dalla proprietà [codecapis \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) .</span><span class="sxs-lookup"><span data-stu-id="5f9e4-111">The meaning of the value of CODECAPI\_AVEncSliceControlSize is controlled by the [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) property.</span></span> <span data-ttu-id="5f9e4-112">La tabella seguente illustra il modo in cui le \_ Proprietà codecapi AVEncSliceControlSize e codecapi \_ AVEncSliceControlMode controllano le dimensioni e il numero di sezioni in un frame.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-112">The following table illustrates how the CODECAPI\_AVEncSliceControlSize and CODECAPI\_AVEncSliceControlMode properties control the size and number of slices in a frame.</span></span>



| <span data-ttu-id="5f9e4-113">Impostazione AVEncSliceControlMode codecapit \_</span><span class="sxs-lookup"><span data-stu-id="5f9e4-113">CODECAPI\_AVEncSliceControlMode setting</span></span> | <span data-ttu-id="5f9e4-114">Significato del valore</span><span class="sxs-lookup"><span data-stu-id="5f9e4-114">Meaning of value</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9e4-115">0</span><span class="sxs-lookup"><span data-stu-id="5f9e4-115">0</span></span>                                       | <span data-ttu-id="5f9e4-116">Si tratta di un numero intero che indica le dimensioni di ogni sezione del frame in unità di macroblocchi.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-116">This is an integer that indicates the size of each slice in the frame in units of macroblocks.</span></span> <br/> <span data-ttu-id="5f9e4-117">Il codificatore deve rifiutare l'impostazione quando il valore è maggiore del numero di macroblocchi nel frame.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-117">The encoder should reject the setting when the value is greater than the number of macroblocks in the frame.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="5f9e4-118">1</span><span class="sxs-lookup"><span data-stu-id="5f9e4-118">1</span></span>                                       | <span data-ttu-id="5f9e4-119">Si tratta di un numero intero che indica le dimensioni di ogni sezione del frame in unità di bit.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-119">This is an integer that indicates the size of each slice in the frame in units of bits.</span></span> <br/> <span data-ttu-id="5f9e4-120">Il codificatore deve avviare una nuova sezione in macroblocco che fa sì che il numero di bit nella sezione superi questo valore (pertanto le dimensioni di ogni sezione saranno sempre minori o uguali a questo valore).</span><span class="sxs-lookup"><span data-stu-id="5f9e4-120">The encoder should start a new slice at the macroblock that causes the number of bits in the slice to exceed this value (so the size of each slice will always be less than or equal than this value).</span></span> <span data-ttu-id="5f9e4-121">Ciò significa che le dimensioni dell'ultima sezione potrebbero essere notevolmente inferiori rispetto a questo valore.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-121">This means that the last slice size could be significantly smaller than this value.</span></span> <br/> |
| <span data-ttu-id="5f9e4-122">2</span><span class="sxs-lookup"><span data-stu-id="5f9e4-122">2</span></span>                                       | <span data-ttu-id="5f9e4-123">Si tratta di un numero intero che indica le dimensioni di ogni sezione del frame in unità di macroblocco righe.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-123">This is an integer that indicates the size of each slice in the frame in units of macroblock rows.</span></span> <br/> <span data-ttu-id="5f9e4-124">Il codificatore deve rifiutare l'impostazione quando il valore è maggiore del numero di righe macroblocco nel frame.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-124">The encoder should reject the setting when the value is greater than the number of macroblock rows in the frame.</span></span><br/>                                                                                                                                                                 |



 

<span data-ttu-id="5f9e4-125">Se l'applicazione non imposta un valore per [CODEcapis \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), il codificatore deve restituire un errore.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-125">If the application does not set a value for [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), the encoder should return an error.</span></span>

<span data-ttu-id="5f9e4-126">Il valore predefinito consigliato consiste nel disporre di una singola sezione per intero frame.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-126">The recommended default is to have a single slice for whole frame.</span></span>

<span data-ttu-id="5f9e4-127">Alcuni codificatori potrebbero codificare le sezioni in parallelo e pertanto le prestazioni potrebbero essere influenzate a seconda delle impostazioni di controllo delle sezioni.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-127">Some encoders might encode slices in parallel and so performance could be affected depending on the slice control settings.</span></span> <span data-ttu-id="5f9e4-128">Ad esempio, la codifica di un frame come una singola sezione potrebbe essere più lenta rispetto a quando il frame è stato codificato come più sezioni.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-128">For example, encoding a frame as a single slice might be slower than if the frame was encoded as multiple slices.</span></span>

<span data-ttu-id="5f9e4-129">Le impostazioni di controllo sezione sono dinamiche e possono essere modificate durante la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="5f9e4-129">The slice control settings are dynamic and can be changed during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f9e4-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f9e4-130">Requirements</span></span>



| <span data-ttu-id="5f9e4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f9e4-131">Requirement</span></span> | <span data-ttu-id="5f9e4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5f9e4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9e4-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f9e4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9e4-134">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5f9e4-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="5f9e4-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f9e4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9e4-136">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5f9e4-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5f9e4-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f9e4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f9e4-138"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f9e4-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f9e4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f9e4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9e4-140">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f9e4-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 





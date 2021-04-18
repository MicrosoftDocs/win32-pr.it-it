---
description: Specifica i coefficienti di riduzione forniti dall'autore per la decodifica dell'audio multicanale per un numero di canali inferiore rispetto al contenuto del flusso codificato.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: Proprietà MFPKEY_WMADEC_FOLDDOWN_MATRIX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309112"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a><span data-ttu-id="f0bbd-103">MFPKEY \_ WMADEC \_ - \_ Proprietà matrice FOLDDOWN</span><span class="sxs-lookup"><span data-stu-id="f0bbd-103">MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX Property</span></span>

<span data-ttu-id="f0bbd-104">Specifica i coefficienti di riduzione forniti dall'autore per la decodifica dell'audio multicanale per un numero di canali inferiore rispetto al contenuto del flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-104">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f0bbd-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f0bbd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f0bbd-106">g \_ wszWMACFoldDownXToYChannels</span><span class="sxs-lookup"><span data-stu-id="f0bbd-106">g\_wszWMACFoldDownXToYChannels</span></span>

<span data-ttu-id="f0bbd-107">g \_ wszWMACFoldXToYChannelsZ</span><span class="sxs-lookup"><span data-stu-id="f0bbd-107">g\_wszWMACFoldXToYChannelsZ</span></span>

## <a name="data-type"></a><span data-ttu-id="f0bbd-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f0bbd-108">Data Type</span></span>

<span data-ttu-id="f0bbd-109">**\_VT array \| VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="f0bbd-109">**VT\_ARRAY \| VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0bbd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0bbd-110">Remarks</span></span>

<span data-ttu-id="f0bbd-111">Un decodificatore audio può fungere da oggetto DMO (DirectX Media Object) o come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="f0bbd-111">An audio decoder can act as a DirectX Media Object (DMO) or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="f0bbd-112">Per informazioni su quando un decodificatore funge da DMO o da un MFT, vedere le pagine di riferimento del singolo codec in [oggetti codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="f0bbd-112">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="f0bbd-113">Quando si utilizza un decodificatore come DMO, il decodificatore è in grado di eseguire la riduzione del canale ed è possibile enumerare i tipi di supporti di output ridotti chiamando [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="f0bbd-113">When you use a decoder as a DMO, the decoder can perform channel fold down, and you can enumerate folded down output media types by calling [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

<span data-ttu-id="f0bbd-114">Quando si usa un decodificatore come MFT, per impostazione predefinita il decodificatore non esegue alcuna riduzione e non offre i tipi di supporti di output ridotti.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-114">When you use a decoder as an MFT, the decoder by default will not perform any fold down, and will not offer folded down output media types.</span></span> <span data-ttu-id="f0bbd-115">Un decodificatore che funge da MFT eseguirà la riduzione solo se vengono impostati coefficienti di riduzioni personalizzati usando la proprietà **MFPKEY \_ WMADEC \_ FOLDDOWN \_ Matrix** .</span><span class="sxs-lookup"><span data-stu-id="f0bbd-115">A decoder acting as an MFT will perform fold down only if custom fold-down coefficients are set using the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property.</span></span>

<span data-ttu-id="f0bbd-116">Se la proprietà della **\_ \_ \_ matrice MFPKEY WMADEC FOLDDOWN** non è impostata sul decodificatore audio MFT e si vuole eseguire una riduzione, è possibile usare (come MFT) il processore del segnale digitale del ricampionatore audio.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-116">If the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property is not set on the audio decoder MFT, and you want to perform a fold down, you can use (as an MFT) the Audio Resampler digital signal processor.</span></span>

<span data-ttu-id="f0bbd-117">Il valore di questa proprietà è una stringa che contiene i coefficienti di riduzione in un elenco delimitato da virgole di valori interi.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-117">The value for this property is a string containing fold-down coefficients in a comma-separated list of integer values.</span></span> <span data-ttu-id="f0bbd-118">L'elenco deve contenere un numero di numeri interi per ogni canale nel contenuto codificato uguale al numero di canali nel contenuto decodificato.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-118">The list must contain a number of integers for each channel in the encoded content equal to the number of channels in the decoded content.</span></span>

<span data-ttu-id="f0bbd-119">Se il coefficiente è zero, il valore da utilizzare nella stringa deve essere "-2147483648". in caso contrario, il valore viene calcolato utilizzando l'equazione: 20 \* 65536 \* log10 (x).</span><span class="sxs-lookup"><span data-stu-id="f0bbd-119">If the coefficient is zero, the value to be used in the string must be "-2147483648";otherwise the value is computed using the equation: 20 \* 65536 \* log10(x).</span></span>

<span data-ttu-id="f0bbd-120">I coefficienti sono elencati nell'ordine della maschera del canale, come definito dalle costanti della maschera di canale incluse nel file di intestazione mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-120">Coefficients are listed in channel mask order, as defined by the channel mask constants that are included in the mmreg.h header file.</span></span> <span data-ttu-id="f0bbd-121">Pertanto, i primi due valori di un canale da 6 a 2 rivolte verso il basso rappresentano le parti del canale di output sinistro e il canale di output destro costituito dal canale sinistro centrale nel flusso del canale 6.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-121">Therefore, the first two values in a 6-to-2 channel fold-down represent the portions of the left output channel and the right output channel that are made up of the center left channel in the 6 channel stream.</span></span>

<span data-ttu-id="f0bbd-122">È necessario impostare questa proprietà solo se i valori di riduzioni specificati dall'autore sono mantenuti con il contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-122">You should set this property only if author-supplied fold-down values are persisted with the encoded content.</span></span> <span data-ttu-id="f0bbd-123">In caso contrario, lasciare che il decodificatore effettui calcoli.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-123">Otherwise, let the decoder make its own calculations.</span></span>

<span data-ttu-id="f0bbd-124">Il codec Windows Media Audio 10 Professional attualmente supporta solo la riduzione a due canali.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-124">The Windows Media Audio 10 Professional codec currently only supports fold-down to two channels.</span></span>

<span data-ttu-id="f0bbd-125">Se la proprietà [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) è impostata su **DSSPEAKER \_ surround**, il codec ignorerà i coefficienti di riduzioni forniti dall'autore e ridurrà a un segnale a 2 canali che può essere elaborato dal decodificatore della matrice del destinatario.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-125">If the [MFPKEY\_WMADEC\_SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) property is set to **DSSPEAKER\_SURROUND**, the codec will ignore author-supplied fold-down coefficients and fold down to a 2-channel signal that can be processed by the matrix decoder of the receiver.</span></span> <span data-ttu-id="f0bbd-126">Ciò consente alle apparecchiature surround di fornire quattro canali.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-126">This enables surround equipment to deliver four channels.</span></span> <span data-ttu-id="f0bbd-127">Questa modalità è supportata solo se l'origine è 5,1.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-127">This mode is supported only if the source is 5.1.</span></span> <span data-ttu-id="f0bbd-128">Il codec può ridurre solo 8 canali a 2 canali.</span><span class="sxs-lookup"><span data-stu-id="f0bbd-128">The codec can only fold 8 channels to 2 channels.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0bbd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0bbd-129">Requirements</span></span>



| <span data-ttu-id="f0bbd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0bbd-130">Requirement</span></span> | <span data-ttu-id="f0bbd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f0bbd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bbd-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0bbd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f0bbd-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f0bbd-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0bbd-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0bbd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f0bbd-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0bbd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0bbd-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0bbd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0bbd-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbd-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0bbd-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0bbd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bbd-139">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0bbd-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

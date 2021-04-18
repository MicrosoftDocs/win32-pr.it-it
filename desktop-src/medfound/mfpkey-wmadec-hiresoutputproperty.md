---
description: Specifica se il decodificatore audio deve fornire un output a risoluzione elevata.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: Proprietà MFPKEY_WMADEC_HIRESOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310266"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a><span data-ttu-id="e60ed-103">MFPKEY \_ WMADEC- \_ Proprietà HIRESOUTPUT</span><span class="sxs-lookup"><span data-stu-id="e60ed-103">MFPKEY\_WMADEC\_HIRESOUTPUT Property</span></span>

<span data-ttu-id="e60ed-104">Specifica se il decodificatore audio deve fornire un output a risoluzione elevata.</span><span class="sxs-lookup"><span data-stu-id="e60ed-104">Specifies whether the audio decoder should deliver high-resolution output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e60ed-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e60ed-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e60ed-106">g \_ wszWMACHiResOutput</span><span class="sxs-lookup"><span data-stu-id="e60ed-106">g\_wszWMACHiResOutput</span></span>

## <a name="data-type"></a><span data-ttu-id="e60ed-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e60ed-107">Data Type</span></span>

<span data-ttu-id="e60ed-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="e60ed-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="e60ed-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="e60ed-109">Default Value</span></span>

<span data-ttu-id="e60ed-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="e60ed-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="e60ed-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e60ed-111">Remarks</span></span>

<span data-ttu-id="e60ed-112">Impostare questa proprietà su VARIANT \_ true per decodificare il contenuto audio multicanale o a 24 bit oppure audio con una frequenza di campionamento superiore a 48.000 Hz.</span><span class="sxs-lookup"><span data-stu-id="e60ed-112">Set this property to VARIANT\_TRUE to decode multichannel or 24-bit audio content, or audio with a sample rate greater than 48,000 Hz.</span></span> <span data-ttu-id="e60ed-113">Se il contenuto è codificato in alta risoluzione, ma questa proprietà è VARIANT \_ false, si applicano i comportamenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e60ed-113">If the content is encoded in high resolution, but this property is VARIANT\_FALSE, the following behaviors apply:</span></span>

-   <span data-ttu-id="e60ed-114">L'output DMO sarà limitato a 16 bit, 48-KHz stereo.</span><span class="sxs-lookup"><span data-stu-id="e60ed-114">The DMO output will be limited to 16-bit, 48-KHz stereo.</span></span>
-   <span data-ttu-id="e60ed-115">Il MFT enumera le modalità di output limitate a 16 bit e non implicano modifiche al numero di canali o alla frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="e60ed-115">The MFT will enumerate output modes that are limited to 16 bits and do not involve changes in channel count or sampling rate.</span></span>

<span data-ttu-id="e60ed-116">Le proprietà dell'audio ad alta risoluzione vengono passate in una struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , non in [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e60ed-116">The properties of high-resolution audio are passed in a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure, not [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span></span>

<span data-ttu-id="e60ed-117">L'output a risoluzione elevata è disponibile solo se il decodificatore è in esecuzione in Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e60ed-117">High-resolution output is available only if the decoder is running on Windows XP or later.</span></span> <span data-ttu-id="e60ed-118">È possibile impostare questa proprietà indipendentemente dal sistema operativo in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e60ed-118">You can set this property regardless of the operating system on which your application is running.</span></span> <span data-ttu-id="e60ed-119">Nelle versioni di Windows precedenti a Windows XP, il decodificatore ignorerà questa impostazione e consegnerà l'output standard.</span><span class="sxs-lookup"><span data-stu-id="e60ed-119">On versions of Windows earlier than Windows XP, the decoder will ignore this setting and deliver standard output.</span></span>

<span data-ttu-id="e60ed-120">Molti lettori (incluso Windows Media Player 9 e versioni successive) impostano questo valore per tutto il contenuto.</span><span class="sxs-lookup"><span data-stu-id="e60ed-120">Many players (including Windows Media Player 9 Series and later) set this value for all content.</span></span>

## <a name="requirements"></a><span data-ttu-id="e60ed-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e60ed-121">Requirements</span></span>



| <span data-ttu-id="e60ed-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e60ed-122">Requirement</span></span> | <span data-ttu-id="e60ed-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e60ed-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e60ed-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e60ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e60ed-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e60ed-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e60ed-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e60ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e60ed-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e60ed-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e60ed-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e60ed-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e60ed-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e60ed-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e60ed-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e60ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60ed-131">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e60ed-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

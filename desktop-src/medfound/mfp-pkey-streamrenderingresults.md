---
description: Specifica i flussi connessi correttamente a un sink multimediale.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: Proprietà MFP_PKEY_StreamRenderingResults (mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343926"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a><span data-ttu-id="49aae-103">\_Proprietà StreamRenderingResults pkey di MFP \_</span><span class="sxs-lookup"><span data-stu-id="49aae-103">MFP\_PKEY\_StreamRenderingResults property</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49aae-104">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="49aae-104">Deprecated.</span></span> <span data-ttu-id="49aae-105">Questa API può essere rimossa dalle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="49aae-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="49aae-106">Le applicazioni devono usare la [sessione multimediale](media-session.md) per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="49aae-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="49aae-107">Specifica i flussi connessi correttamente a un sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="49aae-107">Specifies which streams were connected successfully to a media sink.</span></span>



<span data-ttu-id="49aae-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="49aae-108">Data type</span></span>

<span data-ttu-id="49aae-109">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="49aae-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="49aae-110">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="49aae-110">PROPVARIANT member</span></span>

<span data-ttu-id="49aae-111">Matrice di valori **DWORD** (**Caul**)</span><span class="sxs-lookup"><span data-stu-id="49aae-111">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="49aae-112">VT \_ vettore \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="49aae-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="49aae-113">**CAUL**</span><span class="sxs-lookup"><span data-stu-id="49aae-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="49aae-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="49aae-114">Remarks</span></span>

<span data-ttu-id="49aae-115">Questa proprietà può essere inviata con il **\_ tipo di evento MFP MEDIAITEM evento \_ \_ \_ set** .</span><span class="sxs-lookup"><span data-stu-id="49aae-115">This property can be sent with the **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event.</span></span>

<span data-ttu-id="49aae-116">Il valore della proprietà è una matrice di **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="49aae-116">The value of the property is an array of **HRESULT** s.</span></span> <span data-ttu-id="49aae-117">Le voci della matrice corrispondono ai flussi sull'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="49aae-117">The array entries correspond to streams on the current media item.</span></span> <span data-ttu-id="49aae-118">Ogni voce della matrice indica se il flusso corrispondente è stato connesso a un sink multimediale, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="49aae-118">Each entry in the array indicates whether the corresponding stream was connected to a media sink, as follows:</span></span>

-   <span data-ttu-id="49aae-119">Se il flusso è connesso a un sink multimediale, il valore è **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="49aae-119">If the stream is connected to a media sink, the value is **S\_OK**.</span></span>
-   <span data-ttu-id="49aae-120">Se il flusso non è selezionato, il valore è **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="49aae-120">If the stream is not selected, the value is **S\_FALSE**.</span></span>
-   <span data-ttu-id="49aae-121">Se si è verificato un errore durante il tentativo di connessione del flusso, il valore è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="49aae-121">If an error occurred while attempting to connect the stream, the value is an error code.</span></span>

<span data-ttu-id="49aae-122">Se almeno un flusso è stato connesso correttamente, è possibile eseguire la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="49aae-122">If at least one stream was connected successfully, playback is possible.</span></span> <span data-ttu-id="49aae-123">Ad esempio, l'utente potrebbe avere il codec necessario per riprodurre il flusso audio ma non per riprodurre il flusso video.</span><span class="sxs-lookup"><span data-stu-id="49aae-123">For example, the user might have the codec needed to play the audio stream but not to play the video stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="49aae-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49aae-124">Requirements</span></span>



| <span data-ttu-id="49aae-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="49aae-125">Requirement</span></span> | <span data-ttu-id="49aae-126">Valore</span><span class="sxs-lookup"><span data-stu-id="49aae-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49aae-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49aae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="49aae-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="49aae-128">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="49aae-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49aae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="49aae-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="49aae-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="49aae-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49aae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="49aae-132"><dt>Mfplay. h</dt></span><span class="sxs-lookup"><span data-stu-id="49aae-132"><dt>Mfplay.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49aae-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49aae-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49aae-134">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="49aae-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="49aae-135">**\_ \_ evento set MEDIAITEM \_ MFP**</span><span class="sxs-lookup"><span data-stu-id="49aae-135">**MFP\_MEDIAITEM\_SET\_EVENT**</span></span>](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 





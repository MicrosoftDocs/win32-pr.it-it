---
title: Flag di creazione dell'elenco immagini (Shlobj. h)
description: Set di flag di bit che specifica il tipo di elenco di immagini da creare. Questo parametro può essere una combinazione dei valori seguenti, ma può includere solo uno dei valori di colore ILC \_ . Usato da ImageList \_ create e IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476318"
---
# <a name="image-list-creation-flags"></a><span data-ttu-id="6adac-105">Flag di creazione dell'elenco immagini</span><span class="sxs-lookup"><span data-stu-id="6adac-105">Image List Creation Flags</span></span>

<span data-ttu-id="6adac-106">Set di flag di bit che specifica il tipo di elenco di immagini da creare.</span><span class="sxs-lookup"><span data-stu-id="6adac-106">The set of bit flags that specifies the type of image list to create.</span></span> <span data-ttu-id="6adac-107">Questo parametro può essere una combinazione dei valori seguenti, ma può includere solo uno dei valori di colore ILC \_ .</span><span class="sxs-lookup"><span data-stu-id="6adac-107">This parameter can be a combination of the following values, but it can include only one of the ILC\_COLOR values.</span></span> <span data-ttu-id="6adac-108">Usato da [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span><span class="sxs-lookup"><span data-stu-id="6adac-108">Used by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) and [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span></span>



| <span data-ttu-id="6adac-109">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="6adac-109">Constant/value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="6adac-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6adac-110">Description</span></span>                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <span data-ttu-id="6adac-111"><dt>**ILC \_ MASCHERA**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6adac-111"><dt>**ILC\_MASK**</dt> <dt>0x00000001</dt></span></span> </dl>                                     | <span data-ttu-id="6adac-112">Usare una maschera.</span><span class="sxs-lookup"><span data-stu-id="6adac-112">Use a mask.</span></span> <span data-ttu-id="6adac-113">L'elenco di immagini contiene due bitmap, una delle quali è una bitmap monocromatica utilizzata come maschera.</span><span class="sxs-lookup"><span data-stu-id="6adac-113">The image list contains two bitmaps, one of which is a monochrome bitmap used as a mask.</span></span> <span data-ttu-id="6adac-114">Se questo valore non è incluso, l'elenco di immagini contiene una sola bitmap.</span><span class="sxs-lookup"><span data-stu-id="6adac-114">If this value is not included, the image list contains only one bitmap.</span></span><br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <span data-ttu-id="6adac-115"><dt>**ILC \_**</dt> <dt>0x00000000</dt> colore</span><span class="sxs-lookup"><span data-stu-id="6adac-115"><dt>**ILC\_COLOR**</dt> <dt>0x00000000</dt></span></span> </dl>                                  | <span data-ttu-id="6adac-116">Usare il comportamento predefinito se nessuno degli altri \_ flag COLORx di ILC è specificato.</span><span class="sxs-lookup"><span data-stu-id="6adac-116">Use the default behavior if none of the other ILC\_COLORx flags is specified.</span></span> <span data-ttu-id="6adac-117">In genere, il valore predefinito è ILC \_ COLOR4, ma per i driver di visualizzazione precedenti, il valore predefinito è ILC \_ COLORDDB.</span><span class="sxs-lookup"><span data-stu-id="6adac-117">Typically, the default is ILC\_COLOR4, but for older display drivers, the default is ILC\_COLORDDB.</span></span><br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <span data-ttu-id="6adac-118"><dt>**ILC \_**</dt> <dt>0x000000FE</dt> COLORDDB</span><span class="sxs-lookup"><span data-stu-id="6adac-118"><dt>**ILC\_COLORDDB**</dt> <dt>0x000000FE</dt></span></span> </dl>                         | <span data-ttu-id="6adac-119">Usare una bitmap dipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6adac-119">Use a device-dependent bitmap.</span></span><br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <span data-ttu-id="6adac-120"><dt>**ILC \_**</dt> <dt>0x00000004</dt> COLOR4</span><span class="sxs-lookup"><span data-stu-id="6adac-120"><dt>**ILC\_COLOR4**</dt> <dt>0x00000004</dt></span></span> </dl>                               | <span data-ttu-id="6adac-121">Usare una sezione bitmap (DIB) a 4 bit (a 16 colori) come bitmap per l'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="6adac-121">Use a 4-bit (16-color) device-independent bitmap (DIB) section as the bitmap for the image list.</span></span><br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <span data-ttu-id="6adac-122"><dt>**ILC \_**</dt> <dt>0x00000008</dt> COLOR8</span><span class="sxs-lookup"><span data-stu-id="6adac-122"><dt>**ILC\_COLOR8**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="6adac-123">Usare una sezione DIB a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="6adac-123">Use an 8-bit DIB section.</span></span> <span data-ttu-id="6adac-124">I colori utilizzati per la tabella dei colori sono uguali a quelli della tavolozza dei mezzitoni.</span><span class="sxs-lookup"><span data-stu-id="6adac-124">The colors used for the color table are the same colors as the halftone palette.</span></span><br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <span data-ttu-id="6adac-125"><dt>**ILC \_**</dt> <dt>0x00000010</dt> COLOR16</span><span class="sxs-lookup"><span data-stu-id="6adac-125"><dt>**ILC\_COLOR16**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="6adac-126">Usare una sezione DIB a 16 bit (32/64K-Color).</span><span class="sxs-lookup"><span data-stu-id="6adac-126">Use a 16-bit (32/64k-color) DIB section.</span></span><br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <span data-ttu-id="6adac-127"><dt>**ILC \_**</dt> <dt>0x00000018</dt> COLOR24</span><span class="sxs-lookup"><span data-stu-id="6adac-127"><dt>**ILC\_COLOR24**</dt> <dt>0x00000018</dt></span></span> </dl>                            | <span data-ttu-id="6adac-128">Usare una sezione DIB a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="6adac-128">Use a 24-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <span data-ttu-id="6adac-129"><dt>**ILC \_**</dt> <dt>0x00000020</dt> COLOR32</span><span class="sxs-lookup"><span data-stu-id="6adac-129"><dt>**ILC\_COLOR32**</dt> <dt>0x00000020</dt></span></span> </dl>                            | <span data-ttu-id="6adac-130">Usare una sezione DIB a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6adac-130">Use a 32-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <span data-ttu-id="6adac-131"><dt>**ILC \_ TAVOLOzza**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="6adac-131"><dt>**ILC\_PALETTE**</dt> <dt>0x00000800</dt></span></span> </dl>                            | <span data-ttu-id="6adac-132">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="6adac-132">Not implemented.</span></span><br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <span data-ttu-id="6adac-133"><dt>**ILC \_**</dt> <dt>0x00002000</dt> mirror</span><span class="sxs-lookup"><span data-stu-id="6adac-133"><dt>**ILC\_MIRROR**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="6adac-134">Specchia le icone contenute, se il processo è con mirroring</span><span class="sxs-lookup"><span data-stu-id="6adac-134">Mirror the icons contained, if the process is mirrored</span></span><br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <span data-ttu-id="6adac-135"><dt>**ILC \_**</dt> <dt>0x00008000</dt> PERITEMMIRROR</span><span class="sxs-lookup"><span data-stu-id="6adac-135"><dt>**ILC\_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span></span> </dl>          | <span data-ttu-id="6adac-136">Fa in modo che il codice di mirroring rispecchi ogni elemento quando si inserisce un set di immagini, rispetto all'intera striscia.</span><span class="sxs-lookup"><span data-stu-id="6adac-136">Causes the mirroring code to mirror each item when inserting a set of images, versus the whole strip.</span></span><br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <span data-ttu-id="6adac-137"><dt>**ILC \_**</dt> <dt>0x00010000</dt> ORIGINALSIZE</span><span class="sxs-lookup"><span data-stu-id="6adac-137"><dt>**ILC\_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="6adac-138">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="6adac-138">**Windows Vista and later.**</span></span> <span data-ttu-id="6adac-139">ImageList deve accettare le immagini di set minori di e applicare le dimensioni originali in base all'immagine aggiunta.</span><span class="sxs-lookup"><span data-stu-id="6adac-139">Imagelist should accept smaller than set images and apply original size based on image added.</span></span><br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <span data-ttu-id="6adac-140"><dt>**ILC \_**</dt> <dt>0x00020000</dt> HIGHQUALITYSCALE</span><span class="sxs-lookup"><span data-stu-id="6adac-140"><dt>**ILC\_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="6adac-141">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="6adac-141">**Windows Vista and later.**</span></span> <span data-ttu-id="6adac-142">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6adac-142">Reserved.</span></span><br/>                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="6adac-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6adac-143">Requirements</span></span>



| <span data-ttu-id="6adac-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6adac-144">Requirement</span></span> | <span data-ttu-id="6adac-145">Valore</span><span class="sxs-lookup"><span data-stu-id="6adac-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6adac-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6adac-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6adac-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6adac-147">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6adac-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6adac-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6adac-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6adac-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6adac-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6adac-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6adac-151"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6adac-151"><dt>Shlobj.h</dt></span></span> </dl> |



 

 






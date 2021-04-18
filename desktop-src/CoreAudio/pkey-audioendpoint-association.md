---
description: La \_ proprietà di associazione pkey AudioEndpoint \_ associa una categoria di pin di streaming kernel (KS) a un dispositivo endpoint audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305262"
---
# <a name="pkey_audioendpoint_association"></a><span data-ttu-id="dc29e-103">\_Associazione pkey AudioEndpoint \_</span><span class="sxs-lookup"><span data-stu-id="dc29e-103">PKEY\_AudioEndpoint\_Association</span></span>

<span data-ttu-id="dc29e-104">La proprietà di **\_ \_ associazione pkey AudioEndpoint** associa una categoria di pin di streaming kernel (KS) a un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="dc29e-104">The **PKEY\_AudioEndpoint\_Association** property associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span> <span data-ttu-id="dc29e-105">Il file con estensione inf che installa una scheda audio assegna una categoria pin a ogni pin KS nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="dc29e-105">The .inf file that installs an audio adapter assigns a pin category to each KS pin in the adapter.</span></span> <span data-ttu-id="dc29e-106">Un pin KS in un dispositivo adapter rappresenta il punto in cui un flusso audio entra o esce dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc29e-106">A KS pin on an adapter device represents the point at which an audio stream enters or leaves the device.</span></span> <span data-ttu-id="dc29e-107">Una categoria pin è un GUID che specifica il tipo di funzione eseguita da un pin KS.</span><span class="sxs-lookup"><span data-stu-id="dc29e-107">A pin category is a GUID that specifies the type of function performed by a KS pin.</span></span> <span data-ttu-id="dc29e-108">Ad esempio, il file di intestazione Ksmedia. h definisce il microfono KSNODETYPE GUID della categoria pin \_ per indicare un pin KS che si connette a un microfono e KSNODETYPE le \_ cuffie per indicare un pin KS che si connette alle cuffie.</span><span class="sxs-lookup"><span data-stu-id="dc29e-108">For example, header file Ksmedia.h defines pin-category GUID KSNODETYPE\_MICROPHONE to indicate a KS pin that connects to a microphone, and KSNODETYPE\_HEADPHONES to indicate a KS pin that connects to headphones.</span></span> <span data-ttu-id="dc29e-109">Per ulteriori informazioni, vedere la descrizione delle proprietà della categoria pin nella documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="dc29e-109">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="dc29e-110">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="dc29e-110">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="dc29e-111">Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide a terminazione null che contiene un GUID di categoria del pin KS.</span><span class="sxs-lookup"><span data-stu-id="dc29e-111">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a KS pin category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc29e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc29e-112">Requirements</span></span>



| <span data-ttu-id="dc29e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc29e-113">Requirement</span></span> | <span data-ttu-id="dc29e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="dc29e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc29e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc29e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dc29e-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc29e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dc29e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc29e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dc29e-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc29e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dc29e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc29e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc29e-120"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc29e-120"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc29e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc29e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc29e-122">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="dc29e-122">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="dc29e-123">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="dc29e-123">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 





---
description: La \_ Proprietà pkey AudioEndpoint \_ JackSubType contiene un GUID della categoria di output per un dispositivo endpoint audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127438"
---
# <a name="pkey_audioendpoint_jacksubtype"></a><span data-ttu-id="e7e64-103">PKEY \_ AudioEndpoint \_ JackSubType</span><span class="sxs-lookup"><span data-stu-id="e7e64-103">PKEY\_AudioEndpoint\_JackSubType</span></span>

<span data-ttu-id="e7e64-104">La proprietà **pkey \_ AudioEndpoint \_ JACKSUBTYPE** contiene un GUID della categoria di output per un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="e7e64-104">The **PKEY\_AudioEndpoint\_JackSubType** property contains an output category GUID for an audio endpoint device.</span></span> <span data-ttu-id="e7e64-105">Il file di intestazione Ksmedia. h definisce i GUID; ogni GUID specifica il tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="e7e64-105">The header file Ksmedia.h defines the GUIDs; each GUID specifies the type of connection.</span></span> <span data-ttu-id="e7e64-106">A questi GUID sono inoltre associate categorie pin.</span><span class="sxs-lookup"><span data-stu-id="e7e64-106">These GUIDs also have associated pin categories.</span></span> <span data-ttu-id="e7e64-107">Ad esempio, il file di intestazione Ksmedia. h definisce **l' \_ \_ interfaccia DisplayPort KSNODETYPE** GUID per una porta di visualizzazione che si connette con il pin KS definito dal GUID **PINNAME \_ DisplayPort \_**.</span><span class="sxs-lookup"><span data-stu-id="e7e64-107">For example, header file Ksmedia.h defines the GUID **KSNODETYPE\_DISPLAYPORT\_INTERFACE** for a display port that connects with the KS pin defined by the GUID **PINNAME\_DISPLAYPORT\_OUT**.</span></span>

<span data-ttu-id="e7e64-108">Per ulteriori informazioni, vedere la descrizione delle proprietà della categoria pin nella documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="e7e64-108">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="e7e64-109">Il membro **VT** della struttura **PROPVARIANT** è impostato su **VT \_ LPWSTR**.</span><span class="sxs-lookup"><span data-stu-id="e7e64-109">The **vt** member of the **PROPVARIANT** structure is set to **VT\_LPWSTR**.</span></span>

<span data-ttu-id="e7e64-110">Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide a terminazione null che contiene un GUID di categoria.</span><span class="sxs-lookup"><span data-stu-id="e7e64-110">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e64-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7e64-111">Requirements</span></span>



| <span data-ttu-id="e7e64-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7e64-112">Requirement</span></span> | <span data-ttu-id="e7e64-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e7e64-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e64-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7e64-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e64-115">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7e64-115">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e7e64-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7e64-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e64-117">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7e64-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7e64-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7e64-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7e64-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e64-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e64-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7e64-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e64-121">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="e7e64-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="e7e64-122">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="e7e64-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 





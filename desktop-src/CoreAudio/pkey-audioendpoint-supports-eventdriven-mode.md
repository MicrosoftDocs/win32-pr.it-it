---
description: PKEY \_ AudioEndpoint \_ supporta la \_ proprietà della \_ modalità EventDriven indica se l'endpoint supporta la modalità guidata dagli eventi.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966288"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a><span data-ttu-id="eb523-103">PKEY \_ AudioEndpoint \_ supporta \_ la \_ modalità EventDriven</span><span class="sxs-lookup"><span data-stu-id="eb523-103">PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode</span></span>

<span data-ttu-id="eb523-104">**Pkey AudioEndpoint supporta la proprietà della \_ \_ \_ \_ modalità EventDriven** indica se l'endpoint supporta la modalità guidata dagli eventi.</span><span class="sxs-lookup"><span data-stu-id="eb523-104">The **PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode** property indicates whether the endpoint supports the event-driven mode.</span></span>

<span data-ttu-id="eb523-105">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="eb523-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="eb523-106">Il membro **uintVal** della struttura **PROPVARIANT** è un **valore DWORD** che indica se l'endpoint supporta la modalità guidata dagli eventi.</span><span class="sxs-lookup"><span data-stu-id="eb523-106">The **uintVal** member of the **PROPVARIANT** structure is a **DWORD** that indicates if the endpoint supports the event-driven mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb523-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb523-107">Remarks</span></span>

<span data-ttu-id="eb523-108">Il valore di questa proprietà viene popolato da un OEM audio in un file con estensione inf per indicare che l'hardware HDAudio supporta la modalità guidata dagli eventi in base al requisito WHQL.</span><span class="sxs-lookup"><span data-stu-id="eb523-108">This property value is populated by an audio OEM in an .inf file to indicate that the HDAudio hardware supports event driven mode as per the WHQL requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb523-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb523-109">Requirements</span></span>



| <span data-ttu-id="eb523-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb523-110">Requirement</span></span> | <span data-ttu-id="eb523-111">Valore</span><span class="sxs-lookup"><span data-stu-id="eb523-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb523-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb523-112">Minimum supported client</span></span><br/> | <span data-ttu-id="eb523-113">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eb523-113">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eb523-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb523-114">Minimum supported server</span></span><br/> | <span data-ttu-id="eb523-115">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb523-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb523-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb523-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb523-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb523-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb523-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb523-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb523-119">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="eb523-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="eb523-120">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="eb523-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 





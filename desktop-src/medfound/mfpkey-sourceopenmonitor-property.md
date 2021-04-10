---
description: Contiene un puntatore all'interfaccia IMFSourceOpenMonitor delle applicazioni.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: Proprietà MFPKEY_SourceOpenMonitor (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131226"
---
# <a name="mfpkey_sourceopenmonitor-property"></a><span data-ttu-id="b300f-103">\_Proprietà SourceOpenMonitor di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="b300f-103">MFPKEY\_SourceOpenMonitor property</span></span>

<span data-ttu-id="b300f-104">Contiene un puntatore all'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b300f-104">Contains a pointer to the application's [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>



<span data-ttu-id="b300f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b300f-105">Data type</span></span>

<span data-ttu-id="b300f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="b300f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b300f-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="b300f-107">PROPVARIANT member</span></span>

<span data-ttu-id="b300f-108">Puntatore **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="b300f-108">**IUnknown** pointer</span></span>

<span data-ttu-id="b300f-109">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="b300f-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="b300f-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="b300f-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="b300f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b300f-111">Remarks</span></span>

<span data-ttu-id="b300f-112">Le applicazioni possono passare questa proprietà al resolver di origine per ottenere le notifiche degli eventi dall'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="b300f-112">Applications can pass this property to the source resolver to get event notifications from the network source.</span></span>

## <a name="requirements"></a><span data-ttu-id="b300f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b300f-113">Requirements</span></span>



| <span data-ttu-id="b300f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b300f-114">Requirement</span></span> | <span data-ttu-id="b300f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b300f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b300f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b300f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b300f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b300f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b300f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b300f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b300f-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b300f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b300f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b300f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b300f-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b300f-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b300f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b300f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b300f-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b300f-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 





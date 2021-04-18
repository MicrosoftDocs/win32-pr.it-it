---
description: Valore che indica il tipo di sensore fornito da un'origine frame, ad esempio colore, infrarossi o profondità.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: Attributo MF_MT_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309542"
---
# <a name="mf_mt_framesource_types-attribute"></a><span data-ttu-id="d9077-103">\_ \_ Attributo origine frame di \_ tipo MF mt</span><span class="sxs-lookup"><span data-stu-id="d9077-103">MF\_MT\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="d9077-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="d9077-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d9077-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="d9077-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d9077-106">Valore che indica il tipo di sensore fornito da un'origine frame, ad esempio colore, infrarossi o profondità.</span><span class="sxs-lookup"><span data-stu-id="d9077-106">A value that indicates the type of sensor provided by a frame source, such as color, infrared, or depth.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9077-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d9077-107">Data type</span></span>

<span data-ttu-id="d9077-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d9077-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d9077-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9077-109">Remarks</span></span>

<span data-ttu-id="d9077-110">Questo valore deve essere un membro dell'enumerazione [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d9077-110">This value should be a member of the [**\_MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) enumeration.</span></span> <span data-ttu-id="d9077-111">Per compatibilità con le versioni precedenti, quando questo attributo non è definito in un tipo di supporto, si presuppone che sia **\_ MFFrameSourceTyes:: color**.</span><span class="sxs-lookup"><span data-stu-id="d9077-111">For backward compatibility, when this attribute is not defined on a media type, it's assumed to be **\_MFFrameSourceTyes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9077-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9077-112">Requirements</span></span>



| <span data-ttu-id="d9077-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9077-113">Requirement</span></span> | <span data-ttu-id="d9077-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d9077-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9077-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9077-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d9077-116">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9077-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d9077-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9077-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d9077-118">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9077-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="d9077-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9077-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9077-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9077-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 

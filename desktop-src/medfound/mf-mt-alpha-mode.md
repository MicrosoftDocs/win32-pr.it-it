---
description: Specifica se la modalità Alpha per i tipi di video dei supporti colori è premoltiplicata o diritta.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: Attributo MF_MT_ALPHA_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050095"
---
# <a name="mf_mt_alpha_mode-attribute"></a><span data-ttu-id="c1753-103">\_ \_ Attributo modalità MF mt Alpha \_</span><span class="sxs-lookup"><span data-stu-id="c1753-103">MF\_MT\_ALPHA\_MODE attribute</span></span>

<span data-ttu-id="c1753-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c1753-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c1753-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c1753-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c1753-106">Specifica se la modalità Alpha per i tipi di video dei supporti colori è premoltiplicata o diritta.</span><span class="sxs-lookup"><span data-stu-id="c1753-106">Specifies whether the alpha mode for color media video types is premultiplied or straight.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1753-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c1753-107">Data type</span></span>

<span data-ttu-id="c1753-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c1753-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c1753-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1753-109">Remarks</span></span>

<span data-ttu-id="c1753-110">È possibile eseguire il cast di questo valore in un valore in [**\_ \_ modalità DXGI Alpha**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) .</span><span class="sxs-lookup"><span data-stu-id="c1753-110">This value can be cast to a [**DXGI\_ALPHA\_MODE**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) value.</span></span> <span data-ttu-id="c1753-111">Se questo attributo non è presente, per compatibilità con le versioni precedenti, il valore è **DXGI \_ Alpha \_ mode \_** per il formato video che supporta il canale alfa, ad esempio ARGB32, o **DXGI \_ Alpha \_ mode \_ Ignora** per il formato video senza canale alfa, ad esempio RGB32.</span><span class="sxs-lookup"><span data-stu-id="c1753-111">If this attribute isn’t present, for backward compatibility, the value is **DXGI\_ALPHA\_MODE\_STRAIGHT** for video format supporting alpha channel, such as ARGB32, or **DXGI\_ALPHA\_MODE\_IGNORE** for video format without alpha channel, such as RGB32.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1753-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1753-112">Requirements</span></span>



| <span data-ttu-id="c1753-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1753-113">Requirement</span></span> | <span data-ttu-id="c1753-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c1753-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1753-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1753-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c1753-116">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1753-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c1753-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1753-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c1753-118">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1753-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="c1753-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1753-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1753-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1753-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 

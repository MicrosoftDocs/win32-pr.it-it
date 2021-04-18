---
description: Valore che indica se un frame è stato acquisito usando l'illuminazione a infrarossi attivi (IR).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Attributo MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307977"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a><span data-ttu-id="1d2a7-103">\_ \_ \_ Attributo per l'illuminazione del frame di metadati di acquisizione MF \_</span><span class="sxs-lookup"><span data-stu-id="1d2a7-103">MF\_CAPTURE\_METADATA\_FRAME\_ILLUMINATION attribute</span></span>

<span data-ttu-id="1d2a7-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1d2a7-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1d2a7-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1d2a7-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1d2a7-106">Valore che indica se un frame è stato acquisito usando l'illuminazione a infrarossi attivi (IR).</span><span class="sxs-lookup"><span data-stu-id="1d2a7-106">A value indicating whether a frame was captured using active infrared (IR) illumination.</span></span>

## <a name="data-type"></a><span data-ttu-id="1d2a7-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1d2a7-107">Data type</span></span>

<span data-ttu-id="1d2a7-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1d2a7-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2a7-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d2a7-109">Remarks</span></span>

<span data-ttu-id="1d2a7-110">Questo attributo è una maschera di maschera.</span><span class="sxs-lookup"><span data-stu-id="1d2a7-110">This attribute is a bitmask.</span></span> <span data-ttu-id="1d2a7-111">Si tratta di un valore a 64 bit per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="1d2a7-111">It is a 64 bit value for backward compatibility.</span></span>

<span data-ttu-id="1d2a7-112">L'illuminazione attiva si verifica quando un dispositivo ha un emettitore chiaro vicino alla fotocamera IR che emette un fascio di luce per illuminare la scena, in genere emette luce IR in modo che non disturbi gli occhi umani.</span><span class="sxs-lookup"><span data-stu-id="1d2a7-112">Active illumination is when a device has a light emitter close to the IR camera emitting a beam of light to illuminate the scene, typically emitting IR light so it won’t disturb human eyes.</span></span> <span data-ttu-id="1d2a7-113">Impostare Value su (value & 0x1)! = 0 se frame è stato acquisito quando l'illuminazione attiva era impostata su on e set (value & 0x1) = = 0 se l'illuminazione attiva è disattivata.</span><span class="sxs-lookup"><span data-stu-id="1d2a7-113">Set value to (value & 0x1) != 0 if frame was captured when active illumination was on and set (value & 0x1) == 0 if active illumination was off.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2a7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d2a7-114">Requirements</span></span>



| <span data-ttu-id="1d2a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2a7-115">Requirement</span></span> | <span data-ttu-id="1d2a7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1d2a7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2a7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d2a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2a7-118">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d2a7-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1d2a7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d2a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2a7-120">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d2a7-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="1d2a7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d2a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d2a7-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2a7-122"><dt>Mfapi.h</dt></span></span> </dl> |



 

 





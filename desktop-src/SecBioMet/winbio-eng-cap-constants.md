---
title: Costanti WINBIO_ENG_CAP (tipi WinBio \_ . h)
description: Specificare le funzionalità del motore generico.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743674"
---
# <a name="winbio_eng_cap-constants"></a><span data-ttu-id="4de28-103">\_ \_ Costanti Cap ENG WINBIO</span><span class="sxs-lookup"><span data-stu-id="4de28-103">WINBIO\_ENG\_CAP Constants</span></span>

<span data-ttu-id="4de28-104">Le costanti seguenti sono valori **di \_ capacità WINBIO** che possono essere usati per specificare le funzionalità generiche del componente del motore connesso a un'unità biometrica specifica.</span><span class="sxs-lookup"><span data-stu-id="4de28-104">The following constants are **WINBIO\_CAPABILITIES** values that can be used to specify generic capabilities of the engine component that is connected to a specific biometric unit.</span></span> <span data-ttu-id="4de28-105">Queste funzionalità vengono specificate nel membro **GenericEngineCapabilities** della struttura [**di \_ \_ \_ informazioni del motore esteso di WINBIO**](winbio-extended-engine-info.md) .</span><span class="sxs-lookup"><span data-stu-id="4de28-105">You specify these capabilities in **GenericEngineCapabilities** member of the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure.</span></span>



| <span data-ttu-id="4de28-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="4de28-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="4de28-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4de28-107">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <span data-ttu-id="4de28-108"><dt>**WINBIO \_ 0x00000001 \_ \_ \_ Miglioramento iterativo Cap**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4de28-108"><dt>**WINBIO\_ENG\_CAP\_ITERATIVE\_IMPROVEMENT**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4de28-109">Il componente motore biometrico può eseguire un miglioramento iterativo.</span><span class="sxs-lookup"><span data-stu-id="4de28-109">The biometric engine component can perform iterative improvement.</span></span><br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <span data-ttu-id="4de28-110"><dt>**WINBIO \_ 0x00000002 \_ \_ \_ rilevamento spoofing Cap ENG**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4de28-110"><dt>**WINBIO\_ENG\_CAP\_SPOOF\_DETECTION**</dt> <dt>0x00000002</dt></span></span> </dl>                   | <span data-ttu-id="4de28-111">Il componente motore biometrico può eseguire il rilevamento dello spoofing.</span><span class="sxs-lookup"><span data-stu-id="4de28-111">The biometric engine component can perform spoof detection.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="4de28-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4de28-112">Requirements</span></span>



| <span data-ttu-id="4de28-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4de28-113">Requirement</span></span> | <span data-ttu-id="4de28-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4de28-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4de28-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4de28-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4de28-116">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4de28-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="4de28-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4de28-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4de28-118">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="4de28-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4de28-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4de28-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4de28-120"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4de28-120"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 






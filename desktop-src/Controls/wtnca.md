---
title: Valori WTNCA (uxtheme. h)
description: Specifica i flag che modificano gli attributi dello stile di visualizzazione della finestra. Usare una combinazione bit per bit dei valori seguenti.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121278"
---
# <a name="wtnca-values"></a><span data-ttu-id="9d56d-104">Valori WTNCA</span><span class="sxs-lookup"><span data-stu-id="9d56d-104">WTNCA Values</span></span>

<span data-ttu-id="9d56d-105">Specifica i flag che modificano gli attributi dello stile di visualizzazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="9d56d-105">Specifies flags that modify window visual style attributes.</span></span> <span data-ttu-id="9d56d-106">Usare una combinazione bit per bit dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9d56d-106">Use one, or a bitwise combination of the following values.</span></span>



| <span data-ttu-id="9d56d-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="9d56d-107">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="9d56d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d56d-108">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <span data-ttu-id="9d56d-109"><dt>**WTNCA \_**</dt> <dt>0x00000001</dt> NODRAWCAPTION</span><span class="sxs-lookup"><span data-stu-id="9d56d-109"><dt>**WTNCA\_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="9d56d-110">Impedisce che venga disegnata la didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="9d56d-110">Prevents the window caption from being drawn.</span></span><br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <span data-ttu-id="9d56d-111"><dt>**WTNCA \_**</dt> <dt>0x00000002</dt> NODRAWICON</span><span class="sxs-lookup"><span data-stu-id="9d56d-111"><dt>**WTNCA\_NODRAWICON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="9d56d-112">Impedisce che venga disegnata l'icona del sistema.</span><span class="sxs-lookup"><span data-stu-id="9d56d-112">Prevents the system icon from being drawn.</span></span><br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <span data-ttu-id="9d56d-113"><dt>**WTNCA \_**</dt> <dt>0x00000004</dt> NOSYSMENU</span><span class="sxs-lookup"><span data-stu-id="9d56d-113"><dt>**WTNCA\_NOSYSMENU**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="9d56d-114">Impedisce la visualizzazione del menu icona sistema.</span><span class="sxs-lookup"><span data-stu-id="9d56d-114">Prevents the system icon menu from appearing.</span></span><br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <span data-ttu-id="9d56d-115"><dt>**WTNCA \_**</dt> <dt>0x00000008</dt> NOMIRRORHELP</span><span class="sxs-lookup"><span data-stu-id="9d56d-115"><dt>**WTNCA\_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="9d56d-116">Impedisce il mirroring del punto interrogativo, anche nel layout da destra a sinistra (RTL).</span><span class="sxs-lookup"><span data-stu-id="9d56d-116">Prevents mirroring of the question mark, even in right-to-left (RTL) layout.</span></span><br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <span data-ttu-id="9d56d-117"><dt>**\_VALIDBITS WTNCA**</dt></span><span class="sxs-lookup"><span data-stu-id="9d56d-117"><dt>**WTNCA\_VALIDBITS**</dt></span></span> </dl>                                                                             | <span data-ttu-id="9d56d-118">Maschera che contiene tutti i bit validi.</span><span class="sxs-lookup"><span data-stu-id="9d56d-118">A mask that contains all the valid bits.</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="9d56d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d56d-119">Requirements</span></span>



| <span data-ttu-id="9d56d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d56d-120">Requirement</span></span> | <span data-ttu-id="9d56d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9d56d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d56d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d56d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9d56d-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d56d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9d56d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d56d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9d56d-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d56d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d56d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d56d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d56d-127"><dt>Uxtheme. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d56d-127"><dt>Uxtheme.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d56d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d56d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d56d-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9d56d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9d56d-130">**\_Opzioni WTA**</span><span class="sxs-lookup"><span data-stu-id="9d56d-130">**WTA\_OPTIONS**</span></span>](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[<span data-ttu-id="9d56d-131">**SetWindowThemeNonClientAttributes**</span><span class="sxs-lookup"><span data-stu-id="9d56d-131">**SetWindowThemeNonClientAttributes**</span></span>](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 






---
description: Specifica il tipo di bus di I/O utilizzato dalla scheda grafica.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Enumerazione D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305416"
---
# <a name="d3dbustype-enumeration"></a><span data-ttu-id="6da15-103">Enumerazione D3DBUSTYPE</span><span class="sxs-lookup"><span data-stu-id="6da15-103">D3DBUSTYPE enumeration</span></span>

<span data-ttu-id="6da15-104">Specifica il tipo di bus di I/O utilizzato dalla scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="6da15-104">Specifies the type of I/O bus used by the graphics adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6da15-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a><span data-ttu-id="6da15-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="6da15-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6da15-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ altro**</span><span class="sxs-lookup"><span data-stu-id="6da15-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE\_OTHER**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-108">Indica un tipo di bus diverso dai tipi elencati qui.</span><span class="sxs-lookup"><span data-stu-id="6da15-108">Indicates a type of bus other than the types listed here.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="6da15-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE\_PCI**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-110">Bus PCI.</span><span class="sxs-lookup"><span data-stu-id="6da15-110">PCI bus.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**\_PCIx D3DBUSTYPE**</span><span class="sxs-lookup"><span data-stu-id="6da15-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE\_PCIX**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-112">Bus PCI-X.</span><span class="sxs-lookup"><span data-stu-id="6da15-112">PCI-X bus.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**\_Per D3DBUSTYPE**</span><span class="sxs-lookup"><span data-stu-id="6da15-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE\_PCIEXPRESS**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-114">Bus PCI Express.</span><span class="sxs-lookup"><span data-stu-id="6da15-114">PCI Express bus.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**</span><span class="sxs-lookup"><span data-stu-id="6da15-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE\_AGP**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-116">Bus di porta grafica accelerata (AGP).</span><span class="sxs-lookup"><span data-stu-id="6da15-116">Accelerated Graphics Port (AGP) bus.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Modificatore D3DBUSIMPL \_ all'interno \_ del \_ chipset**</span><span class="sxs-lookup"><span data-stu-id="6da15-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL\_MODIFIER\_INSIDE\_OF\_CHIPSET**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-118">L'implementazione per la scheda grafica si trova nel Bridge nord di un chipset della scheda madre.</span><span class="sxs-lookup"><span data-stu-id="6da15-118">The implementation for the graphics adapter is in a motherboard chipset's north bridge.</span></span> <span data-ttu-id="6da15-119">Questo flag implica che i dati non passano mai su un bus di espansione (ad esempio, PCI o AGP) quando viene trasferito dalla memoria principale alla scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="6da15-119">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**\_Il modificatore D3DBUSIMPL \_ tiene traccia della \_ \_ \_ scheda madre per il \_ \_ chip**</span><span class="sxs-lookup"><span data-stu-id="6da15-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_CHIP**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-121">Indica che la scheda grafica è connessa al Bridge nord di un chipset della scheda madre mediante tracce sulla scheda madre e che tutti i chip della scheda grafica sono saldati alla scheda madre.</span><span class="sxs-lookup"><span data-stu-id="6da15-121">Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard.</span></span> <span data-ttu-id="6da15-122">Questo flag implica che i dati non passano mai su un bus di espansione (ad esempio, PCI o AGP) quando viene trasferito dalla memoria principale alla scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="6da15-122">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**\_Il modificatore D3DBUSIMPL \_ tiene traccia della \_ \_ \_ scheda madre \_ al \_ socket**</span><span class="sxs-lookup"><span data-stu-id="6da15-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_SOCKET**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-124">La scheda grafica è connessa al Bridge nord di un chipset della scheda madre mediante tracce sulla scheda madre e tutti i chip della scheda grafica sono connessi tramite socket alla scheda madre.</span><span class="sxs-lookup"><span data-stu-id="6da15-124">The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_Connettore della \_ \_ scheda figlia del modificatore D3DBUSIMPL \_**</span><span class="sxs-lookup"><span data-stu-id="6da15-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-126">La scheda grafica è connessa alla scheda madre tramite un connettore daughterboard.</span><span class="sxs-lookup"><span data-stu-id="6da15-126">The graphics adapter is connected to the motherboard through a daughterboard connector.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**Connettore D3DBUSIMPL per \_ \_ la figlia del modificatore \_ \_ \_ all'interno \_ di \_ NUAE**</span><span class="sxs-lookup"><span data-stu-id="6da15-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR\_INSIDE\_OF\_NUAE**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-128">La scheda grafica è connessa alla scheda madre tramite un connettore daughterboard e la scheda grafica si trova all'interno di un'enclosure non accessibile dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6da15-128">The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.</span></span>

</dd> <dt>

<span data-ttu-id="6da15-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificatore D3DBUSIMPL \_ non \_ standard**</span><span class="sxs-lookup"><span data-stu-id="6da15-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL\_MODIFIER\_NON\_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="6da15-130">Viene impostato uno dei flag di modifica D3DBUSIMPL del modificatore \_ \_ \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="6da15-130">One of the D3DBUSIMPL\_MODIFIER\_MODIFIER\_Xxx flags is set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6da15-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="6da15-131">Remarks</span></span>

<span data-ttu-id="6da15-132">È possibile impostare un numero di tre flag.</span><span class="sxs-lookup"><span data-stu-id="6da15-132">As many as three flags can be set.</span></span> <span data-ttu-id="6da15-133">I flag compresi nell'intervallo da 0x00 a 0x04 (**D3DBUSTYPE \_ xxx**) forniscono il tipo di bus di base.</span><span class="sxs-lookup"><span data-stu-id="6da15-133">Flags in the range 0x00 through 0x04 (**D3DBUSTYPE\_Xxx**) provide the basic bus type.</span></span> <span data-ttu-id="6da15-134">I flag nell'intervallo compreso tra 0x10000 e 0x50000 (**\_ modificatore D3DBUSIMPL \_ xxx**) modificano la descrizione di base.</span><span class="sxs-lookup"><span data-stu-id="6da15-134">Flags in the range 0x10000 through 0x50000 (**D3DBUSIMPL\_MODIFIER\_Xxx**) modify the basic description.</span></span> <span data-ttu-id="6da15-135">Il driver imposta un flag di tipo bus e può impostare zero o un flag di modifica.</span><span class="sxs-lookup"><span data-stu-id="6da15-135">The driver sets one bus-type flag, and can set zero or one modifier flag.</span></span> <span data-ttu-id="6da15-136">Se il driver imposta un flag di modifica, imposta anche il **flag \_ \_ non \_ standard del modificatore D3DBUSIMPL** .</span><span class="sxs-lookup"><span data-stu-id="6da15-136">If the driver sets a modifier flag, it also sets the **D3DBUSIMPL\_MODIFIER\_NON\_STANDARD** flag.</span></span> <span data-ttu-id="6da15-137">I flag vengono combinati con un **or** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="6da15-137">Flags are combined with a bitwise **OR**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6da15-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6da15-138">Requirements</span></span>



| <span data-ttu-id="6da15-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6da15-139">Requirement</span></span> | <span data-ttu-id="6da15-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6da15-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da15-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6da15-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6da15-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6da15-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6da15-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6da15-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6da15-144">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6da15-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6da15-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6da15-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6da15-146"><dt>D3d9types. h (include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6da15-146"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da15-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6da15-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da15-148">Enumerazioni video Direct3D</span><span class="sxs-lookup"><span data-stu-id="6da15-148">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 





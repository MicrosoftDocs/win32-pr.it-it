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
# <a name="d3dbustype-enumeration"></a>Enumerazione D3DBUSTYPE

Specifica il tipo di bus di I/O utilizzato dalla scheda grafica.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ altro**
</dt> <dd>

Indica un tipo di bus diverso dai tipi elencati qui.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
</dt> <dd>

Bus PCI.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**\_PCIx D3DBUSTYPE**
</dt> <dd>

Bus PCI-X.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**\_Per D3DBUSTYPE**
</dt> <dd>

Bus PCI Express.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

Bus di porta grafica accelerata (AGP).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Modificatore D3DBUSIMPL \_ all'interno \_ del \_ chipset**
</dt> <dd>

L'implementazione per la scheda grafica si trova nel Bridge nord di un chipset della scheda madre. Questo flag implica che i dati non passano mai su un bus di espansione (ad esempio, PCI o AGP) quando viene trasferito dalla memoria principale alla scheda grafica.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**\_Il modificatore D3DBUSIMPL \_ tiene traccia della \_ \_ \_ scheda madre per il \_ \_ chip**
</dt> <dd>

Indica che la scheda grafica è connessa al Bridge nord di un chipset della scheda madre mediante tracce sulla scheda madre e che tutti i chip della scheda grafica sono saldati alla scheda madre. Questo flag implica che i dati non passano mai su un bus di espansione (ad esempio, PCI o AGP) quando viene trasferito dalla memoria principale alla scheda grafica.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**\_Il modificatore D3DBUSIMPL \_ tiene traccia della \_ \_ \_ scheda madre \_ al \_ socket**
</dt> <dd>

La scheda grafica è connessa al Bridge nord di un chipset della scheda madre mediante tracce sulla scheda madre e tutti i chip della scheda grafica sono connessi tramite socket alla scheda madre.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_Connettore della \_ \_ scheda figlia del modificatore D3DBUSIMPL \_**
</dt> <dd>

La scheda grafica è connessa alla scheda madre tramite un connettore daughterboard.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**Connettore D3DBUSIMPL per \_ \_ la figlia del modificatore \_ \_ \_ all'interno \_ di \_ NUAE**
</dt> <dd>

La scheda grafica è connessa alla scheda madre tramite un connettore daughterboard e la scheda grafica si trova all'interno di un'enclosure non accessibile dall'utente.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificatore D3DBUSIMPL \_ non \_ standard**
</dt> <dd>

Viene impostato uno dei flag di modifica D3DBUSIMPL del modificatore \_ \_ \_ xxx.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile impostare un numero di tre flag. I flag compresi nell'intervallo da 0x00 a 0x04 (**D3DBUSTYPE \_ xxx**) forniscono il tipo di bus di base. I flag nell'intervallo compreso tra 0x10000 e 0x50000 (**\_ modificatore D3DBUSIMPL \_ xxx**) modificano la descrizione di base. Il driver imposta un flag di tipo bus e può impostare zero o un flag di modifica. Se il driver imposta un flag di modifica, imposta anche il **flag \_ \_ non \_ standard del modificatore D3DBUSIMPL** . I flag vengono combinati con un **or** bit per bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h (include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni video Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 





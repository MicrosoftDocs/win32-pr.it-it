---
description: Specifica il tipo di bus di I/O utilizzato dalla scheda grafica.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Enumerazione D3DBUSTYPE (D3d9types.h)
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
ms.openlocfilehash: cece215946406bedcca2cbfdd2b64bfdb5df00208b2d84cf2aa90fdb89b516bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828381"
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

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ OTHER**
</dt> <dd>

Indica un tipo di bus diverso da quelli elencati di seguito.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
</dt> <dd>

Bus PCI.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**
</dt> <dd>

Bus PCI-X.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**
</dt> <dd>

Bus PCI Express.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

Bus AGP (Accelerated Graphics Port).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**MODIFICATORE D3DBUSIMPL \_ \_ \_ ALL'INTERNO DEL \_ CHIPSET**
</dt> <dd>

L'implementazione per la scheda grafica si trova nel ponte nord di un chipset della scheda madre. Questo flag implica che i dati non passano mai attraverso un bus di espansione (ad esempio PCI o AGP) quando vengono trasferiti dalla memoria principale alla scheda grafica.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**TRACCE MODIFICATORI D3DBUSIMPL \_ SULLA SCHEDA MADRE PER \_ \_ \_ \_ \_ \_ CHIP**
</dt> <dd>

Indica che la scheda grafica è connessa al ponte nord di un chipset della scheda madre tramite tracce sulla scheda madre e che tutti i chip della scheda grafica vengono venduti alla scheda madre. Questo flag implica che i dati non passano mai attraverso un bus di espansione (ad esempio PCI o AGP) quando vengono trasferiti dalla memoria principale alla scheda grafica.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**TRACCE MODIFICATORI D3DBUSIMPL \_ SULLA SCHEDA MADRE PER IL \_ \_ \_ \_ \_ \_ SOCKET**
</dt> <dd>

La scheda grafica è connessa al ponte nord di un chipset della scheda madre tramite tracce sulla scheda madre e tutti i chip della scheda grafica sono connessi tramite socket alla scheda madre.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL \_ MODIFIER \_ DAUGHTER \_ BOARD \_ CONNECTOR**
</dt> <dd>

La scheda grafica è connessa alla scheda madre tramite un connettore della scheda madre.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL \_ MODIFIER DAUGHTER BOARD CONNECTOR \_ \_ \_ \_ \_ ALL'INTERNO DI \_ NUAE**
</dt> <dd>

La scheda grafica è connessa alla scheda madre tramite un connettore della scheda madre e la scheda grafica si trova all'interno di uno chassis non accessibile dall'utente.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**MODIFICATORE D3DBUSIMPL \_ \_ NON \_ STANDARD**
</dt> <dd>

Uno dei flag D3DBUSIMPL \_ MODIFIER MODIFIER Xxx è \_ \_ impostato.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile impostare un numero di tre flag. I flag nell'intervallo 0x00 da 0x04 (**D3DBUSTYPE \_ Xxx**) forniscono il tipo di bus di base. I flag nell'intervallo 0x10000 a 0x50000 (**D3DBUSIMPL \_ MODIFIER \_ Xxx**) modificano la descrizione di base. Il driver imposta un flag di tipo bus e può impostare zero o un flag di modifica. Se il driver imposta un flag di modifica, imposta anche il flag **D3DBUSIMPL \_ MODIFIER \_ NON \_ STANDARD.** I flag vengono combinati con or bit per **bit.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types.h (includere D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni video Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 





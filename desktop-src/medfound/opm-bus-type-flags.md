---
description: I flag elencati nella tabella seguente specificano il tipo di bus di I/O utilizzato dalla scheda grafica.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: Flag di tipo del bus OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae3e6988d6bcd33015b0efc5b12561ef3373a9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527894"
---
# <a name="opm-bus-type-flags"></a>Flag di tipo bus OPM

I flag elencati nella tabella seguente specificano il tipo di bus di I/O utilizzato dalla scheda grafica.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ \_Tipo bus \_ altri**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Indica un tipo di bus diverso dai tipi elencati qui.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ Tipo BUS 0x00000001 \_ \_ PCI**</dt> <dt></dt> </dl>                                                                                                                                                                            | Bus PCI.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ Tipo di BUS \_ \_ PCIx**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | Bus PCI-X.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ Tipo di BUS \_ \_ per**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | Bus PCI Express.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ \_Tipo bus \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | Bus di porta grafica accelerata (AGP).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ \_ \_ Modificatore \_ di implementazione del bus all'interno \_ del \_ chipset**</dt> <dt>0x00010000</dt> </dl>                                                                      | L'implementazione per la scheda grafica si trova nel Bridge nord di un chipset della scheda madre. Questo flag implica che i dati non passano mai su un bus di espansione (ad esempio, PCI o AGP) quando viene trasferito dalla memoria principale alla scheda grafica. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ \_ \_ Il modificatore \_ di implementazione del bus tiene traccia della \_ \_ \_ scheda madre per il \_ \_ chip**</dt> <dt>0x00020000</dt> </dl>                            | La scheda grafica è connessa al Bridge nord di un chipset della scheda madre mediante tracce sulla scheda madre e tutti i chip della scheda grafica (circuiti integrati) vengono saldati alla scheda madre. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ \_ \_ Il modificatore \_ di implementazione del bus tiene traccia della \_ \_ \_ scheda madre \_ per 0x00030000 \_ socket**</dt> <dt></dt> </dl>                      | La scheda grafica è connessa al Bridge nord di un chipset della scheda madre mediante tracce sulla scheda madre e tutti i chip della scheda grafica sono connessi tramite socket alla scheda madre.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ Connettore di implementazione del BUS \_ figlia del \_ \_ \_ \_ connettore della lavagna**</dt> <dt>0x00040000</dt> </dl>                                                 | La scheda grafica è connessa alla scheda madre tramite un connettore daughterboard.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ \_Connettore di implementazione del bus, il \_ \_ \_ \_ connettore di scheda figlio \_ all'interno \_ di \_ NUAE**</dt> <dt>0x00050000</dt> </dl> | La scheda grafica è connessa alla scheda madre tramite un connettore daughterboard e la scheda grafica si trova all'interno di un'enclosure non accessibile dall'utente.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ \_Modificatore di implementazione bus \_ \_ non \_ standard**</dt> <dt>0x80000000</dt> </dl>                                                                                      | Modificatore non standard. Facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ 0x80000000 \_ \_ integrato di \_ tipo \_ bus Copp compatibile**</dt> <dt></dt> </dl>                                                                                                     | Bus integrato. Questo flag viene usato solo in modalità di emulazione COPP. Indica che i segnali di stato e di comando tra la scheda grafica e gli altri sottosistemi del computer non sono disponibili in un bus di espansione con una specifica pubblica e un tipo di connettore standard, a meno che non si tratti di un bus di memoria. Questo flag può essere combinato con un flag di **\_ \_ tipo \_ xxx del bus OPM** .<br/> |



## <a name="remarks"></a>Commenti

È possibile impostare fino a tre flag utilizzando **un operatore OR** bit per bit. I flag compresi nell'intervallo da 0x00 a 0x04 (**\_ tipo di bus OPM \_ \_ xxx**) forniscono il tipo di bus di base. I flag nell'intervallo 0x10000 tramite 0x50000 (**\_ \_ \_ modificatore di implementazione \_ del bus OPM xxx**) modificano la descrizione di base. Il driver imposta un flag di tipo bus e può facoltativamente impostare un flag per un solo modificatore. Inoltre, il driver può facoltativamente impostare il flag **di \_ implementazione del bus OPM \_ \_ \_ non \_ standard** .

In modalità di emulazione COPP, il driver non usa i flag di modifica, ma potrebbe impostare il **flag \_ \_ integrato del \_ \_ tipo \_ di bus compatibile con copp di OPM** .

I \_ flag di \_ tipo \_ di bug di OPM xxxx e il flag **integrato del \_ \_ \_ \_ tipo \_ di bus compatibile con copp di OPM** sono equivalenti ai valori dell'enumerazione [**\_ BusType di Copp**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) utilizzata in Certified Output Protocol (Copp).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di OPM](opm-enumerations.md)
</dt> </dl>

 

 

---
description: I flag elencati nella tabella seguente specificano il tipo di bus di I/O usato dalla scheda grafica.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: Flag di tipo bus OPM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4989a91c308a7dc82bb15e9cd577a6facd89a0a6de9a32f0ef95f400917ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973000"
---
# <a name="opm-bus-type-flags"></a>Flag di tipo bus OPM

I flag elencati nella tabella seguente specificano il tipo di bus di I/O usato dalla scheda grafica.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ BUS \_ TYPE \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Indica un tipo di bus diverso da quelli elencati di seguito.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ BUS \_ DI TIPO \_ PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | Bus PCI.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ BUS \_ DI TIPO \_ PCIX**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | Bus PCI-X.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ TIPO \_ DI \_ BUS PCIEXPRESS**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | Bus PCI Express.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ Bus \_ TYPE \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | Bus AGP (Accelerated Graphics Port).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ MODIFICATORE DI IMPLEMENTAZIONE DEL BUS \_ \_ \_ \_ ALL'INTERNO \_**</dt> DI CHIPSET <dt>0X00010000</dt> </dl>                                                                      | L'implementazione per la scheda grafica si trova nel bridge nord di un chipset della scheda madre. Questo flag implica che i dati non passano mai attraverso un bus di espansione (ad esempio PCI o AGP) quando vengono trasferiti dalla memoria principale alla scheda grafica. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ IL \_ MODIFICATORE DI IMPLEMENTAZIONE DEL BUS \_ TIENE TRACCIA DELLA SCHEDA MADRE IN \_ \_ \_ \_ \_ \_ CHIP**</dt> <dt>0X00020000</dt> </dl>                            | La scheda grafica è connessa al bridge nord di un chipset della scheda madre tramite tracce sulla scheda madre e tutti i chip della scheda grafica (circuiti integrati) vengono venduti alla scheda madre. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ IL \_ MODIFICATORE DI IMPLEMENTAZIONE DEL BUS \_ TIENE TRACCIA SULLA SCHEDA MADRE PER IL \_ \_ \_ \_ \_ \_ 0X00030000**</dt> <dt></dt> </dl>                      | La scheda grafica è connessa al bridge nord di un chipset della scheda madre tramite tracce sulla scheda madre e tutti i chip della scheda grafica sono connessi tramite socket alla scheda madre.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ CONNETTORE \_ BOARD \_ DEL \_ \_ MODIFICATORE DI \_ IMPLEMENTAZIONE BUS 0X00040000**</dt> <dt></dt> </dl>                                                 | La scheda grafica è connessa alla scheda madre tramite un connettore della scheda madre.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ CONNETTORE \_ \_ BOARD DEL \_ \_ MODIFICATORE DI \_ IMPLEMENTAZIONE BUS \_ \_ ALL'INTERNO DI \_ NUAE**</dt> <dt>0X00050000</dt> </dl> | La scheda grafica è connessa alla scheda madre tramite un connettore della scheda madre e la scheda grafica si trova all'interno di uno chassis non accessibile dall'utente.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ MODIFICATORE \_ DI \_ \_ IMPLEMENTAZIONE DEL BUS NON \_ STANDARD**</dt> <dt>0X80000000</dt> </dl>                                                                                      | Modificatore non standard. Facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ TIPO DI BUS INTEGRATO COMPATIBILE CON COPP \_ \_ \_ \_ 0X80000000**</dt> <dt></dt> </dl>                                                                                                     | Bus integrato. Questo flag viene usato solo in modalità di emulazione COPP. Indica che i segnali di comando e stato tra la scheda grafica e altri sottosistemi nel computer non sono disponibili in un bus di espansione con una specifica pubblica e un tipo di connettore standard, a meno che non si tratta di un bus di memoria. Questo flag può essere combinato con un flag **OPM \_ BUS TYPE \_ \_ Xxx.**<br/> |



## <a name="remarks"></a>Commenti

È possibile impostare fino a tre flag, usando **un'operazione OR** bit per bit. I flag nell'intervallo 0x00 a 0x04 (**OPM \_ BUS TYPE \_ \_ Xxx**) forniscono il tipo di bus di base. I flag nell'intervallo da 0x10000 a 0x50000 (**OPM \_ BUS IMPLEMENTATION MODIFIER \_ \_ \_ Xxx**) modificano la descrizione di base. Il driver imposta un flag di tipo bus e, facoltativamente, può impostare un solo flag di modifica. Inoltre, il driver può facoltativamente impostare il flag **OPM \_ BUS IMPLEMENTATION MODIFIER NON \_ \_ \_ \_ STANDARD.**

In modalità di emulazione COPP, il driver non usa i flag di modifica, ma potrebbe impostare il flag **OPM \_ COPP \_ COMPATIBLE \_ BUS TYPE \_ \_ INTEGRATED.**

I flag OPM BUG TYPE Xxxx e \_ OPM COPP COMPATIBLE BUS TYPE INTEGRATED sono equivalenti ai valori dell'enumerazione \_ \_ [**\_ CoPP BusType**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) usata in Certified Output Protection Protocol (COPP). **\_ \_ \_ \_ \_**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni OPM](opm-enumerations.md)
</dt> </dl>

 

 

---
description: Restituisce il tipo di bus di I/O usato dall'output del video.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309059"
---
# <a name="opm_get_adapter_bus_type"></a>\_tipo di \_ bus di adapter \_ \_ per OPM Get

Restituisce il tipo di bus di I/O usato dall'output del video.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------|
| GUID richiesta | \_tipo di \_ bus di adapter \_ \_ per OPM Get                                                |
| Dati di input   | nessuno                                                                        |
| Restituisce i dati  | Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Commenti

Il tipo di bus viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Il valore è **un operatore OR** bit per bit di flag di [**tipo bus OPM**](opm-bus-type-flags.md).

Questa query equivale alla \_ query DXVA COPPQueryBusData utilizzata in Certified Output Protocol (Copp).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato di OPM](opm-status-requests.md)
</dt> </dl>

 

 





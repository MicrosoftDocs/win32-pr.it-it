---
description: Restituisce il tipo di connettore fisico dell'output del video.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226521"
---
# <a name="opm_get_connector_type"></a>\_tipo di \_ connettore OPM Get \_

Restituisce il tipo di connettore fisico dell'output del video.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------|
| GUID richiesta | \_tipo di \_ connettore OPM Get \_                                                   |
| Dati di input   | nessuno                                                                        |
| Restituisce i dati  | Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Commenti

Il tipo di connettore viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Il valore di **ulInformation** è uguale a uno dei tipi di connettore elencati nei [**flag di tipo del connettore OPM**](opm-connector-type-flags.md).

In modalità di emulazione COPP, il tipo di connettore può essere combinato con il flag **interno del tipo di connettore di OPM \_ Copp \_ compatibile \_ \_ \_** . Usare un operatore **and** bit per bit per estrarre il tipo di connettore:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Le applicazioni devono ignorare il flag **\_ interno del \_ \_ \_ tipo \_ di connettore con compatibilità OPM Copp** . Per ulteriori informazioni, vedere la sezione Osservazioni dei [**flag del tipo di connettore OPM**](opm-connector-type-flags.md).

Questa query equivale alla \_ query DXVA COPPQueryConnectorType utilizzata in Certified Output Protocol (Copp).

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

 

 





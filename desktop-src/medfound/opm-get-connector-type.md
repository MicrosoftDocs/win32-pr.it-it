---
description: Restituisce il tipo di connettore fisico dell'output video.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099da66193048b52011e58eb5ce3f925d451fc1ad26b193f2955f6012f0e607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887501"
---
# <a name="opm_get_connector_type"></a>OPM \_ GET \_ CONNECTOR \_ TYPE

Restituisce il tipo di connettore fisico dell'output video.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------|
| GUID richiesta | OPM \_ GET \_ CONNECTOR \_ TYPE                                                   |
| Dati di input   | Nessuno                                                                        |
| Restituisce i dati  | Struttura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Commenti

Il tipo di connettore viene restituito nel **membro ulInformation** della [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Il valore di **ulInformation** è uguale a uno dei tipi di connettore elencati in [**Flag dei tipi di connettore OPM**](opm-connector-type-flags.md).

In modalità di emulazione COPP, il tipo di connettore potrebbe essere combinato con il flag **OPM \_ COPP \_ COMPATIBLE \_ CONNECTOR TYPE \_ \_ INTERNAL.** Usare un'operazione **AND** bit per bit per estrarre il tipo di connettore:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Le applicazioni devono ignorare il flag **OPM \_ COPP \_ COMPATIBLE \_ CONNECTOR TYPE \_ \_ INTERNAL.** Per altre informazioni, vedere la sezione Osservazioni in Flag dei tipi di [**connettore OPM.**](opm-connector-type-flags.md)

Questa query equivale alla \_ query DXVA COPPQueryConnectorType usata in Certified Output Protection Protocol (COPP).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato OPM](opm-status-requests.md)
</dt> </dl>

 

 





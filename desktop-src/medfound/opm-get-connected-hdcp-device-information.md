---
description: 'Altre informazioni su: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d692680e6492a3dc5d92073baf069eefffde68841925ced9afd69dde4d5fcd97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239894"
---
# <a name="opm_get_connected_hdcp_device_information"></a>OPM \_ GET CONNECTED HDCP DEVICE INFORMATION (OTTENERE \_ INFORMAZIONI SUL DISPOSITIVO \_ HDCP \_ \_ CONNESSO)

Ottiene informazioni su High-Bandwidth dispositivo HDCP (Digital protezione del contenuto) collegato all'output video. Vengono restituite le informazioni seguenti:

-   Vettore di selezione della chiave HDCP (KSV) del dispositivo.
-   Indica se il dispositivo è un ripetitore HDCP.



| Requisito | Valore |
|--------------|---------------------------------------------------------------------------------------------------------|
| GUID richiesta | OPM \_ GET CONNECTED HDCP DEVICE INFORMATION (OTTENERE \_ INFORMAZIONI SUL DISPOSITIVO \_ HDCP \_ \_ CONNESSO)                                                          |
| Dati di input   | Nessuno                                                                                                    |
| Restituisce i dati  | Struttura [**OPM \_ CONNECTED \_ HDCP DEVICE \_ \_ INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Commenti

Questa query può essere usata solo con la *modalità di emulazione COPP*. Se [**l'interfaccia IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usa la semantica di Output Protection Manager (OPM), questa richiesta di stato non è supportata.

La KSV è un identificatore fornito al produttore del dispositivo e viene usata nel processo di autenticazione e configurazione HDCP. In modalità di emulazione COPP, l'applicazione usa la chiave di distribuzione della chiave per determinare se il dispositivo HDCP è revocato. In caso contrario, l'applicazione non deve riprodurre contenuto protetto. Inoltre, l'applicazione non deve riprodurre contenuto protetto se il dispositivo è un ripetitore HDCP, perché COPP non supporta i ripetitori HDCP.

Questa query non è necessaria quando si usa la semantica OPM, perché OPM supporta la revoca del dispositivo e i ripetitori HDCP.

Questa query è equivalente alla \_ query DXVA COPPQueryHDCPKeyData usata in Certified Output Protection Protocol (COPP).

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

[Richieste di stato OPM](opm-status-requests.md)
</dt> </dl>

 

 





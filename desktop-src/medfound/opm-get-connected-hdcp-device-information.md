---
description: 'Altre informazioni su: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527883"
---
# <a name="opm_get_connected_hdcp_device_information"></a>\_ \_ \_ \_ informazioni sul dispositivo HDCP connesso \_ ad OPM

Ottiene informazioni su un dispositivo High-Bandwidth Digital protezione del contenuto (HDCP) collegato all'output del video. Vengono restituite le seguenti informazioni:

-   Il vettore di selezione della chiave HDCP del dispositivo (KSV).
-   Indica se il dispositivo è un ripetitore HDCP.



| Requisito | Valore |
|--------------|---------------------------------------------------------------------------------------------------------|
| GUID richiesta | \_ \_ \_ \_ informazioni sul dispositivo HDCP connesso \_ ad OPM                                                          |
| Dati di input   | nessuno                                                                                                    |
| Restituisce i dati  | Struttura [**di \_ \_ \_ \_ informazioni sul dispositivo HDCP connesso a OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Commenti

Questa query può essere utilizzata solo con la *modalità di emulazione Copp*. Se l'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usa la semantica di output Protection Manager (OPM), questa richiesta di stato non è supportata.

KSV è un identificatore fornito al produttore del dispositivo e viene usato nel processo di autenticazione e configurazione di HDCP. In modalità di emulazione COPP, l'applicazione usa il KSV per determinare se il dispositivo HDCP è stato revocato. In caso contrario, l'applicazione non deve riprodurre contenuto protetto. Inoltre, l'applicazione non deve riprodurre contenuto protetto se il dispositivo è un ripetitore HDCP, perché COPP non supporta i ripetitori HDCP.

Questa query non è necessaria quando viene usata la semantica di OPM, perché OPM supporta le revoche di dispositivi e i ripetitori HDCP.

Questa query equivale alla \_ query DXVA COPPQueryHDCPKeyData utilizzata in Certified Output Protocol (Copp).

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

[Richieste di stato di OPM](opm-status-requests.md)
</dt> </dl>

 

 





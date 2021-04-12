---
description: Ottiene il valore di Merit di un codec hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226522"
---
# <a name="opm_get_codec_info"></a>\_informazioni sul \_ codec di Get di OPM \_

Ottiene il valore di Merit di un codec hardware.



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------------|
| GUID richiesta | **\_informazioni sul \_ codec di Get di OPM \_**                                                                 |
| Dati di input   | Una struttura di [**\_ parametri di \_ \_ informazioni \_ sul codec Get di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Restituisce i dati  | Struttura [**di \_ \_ \_ \_ informazioni sul codec Get di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Commenti

Sebbene questo comando usi l'interfaccia di [Output Protection Manager](output-protection-manager.md) (OPM), si applica solo a codificatori e decodificatori hardware. Non si applica ai dispositivi di output video.

In genere, non usare direttamente questo comando. Per ottenere il valore di Merit per un codec hardware, chiamare la funzione [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) . Questa funzione esegue tutte le chiamate OPM necessarie per inviare il comando **OPM \_ get \_ codec \_ info** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Richieste di stato di OPM](opm-status-requests.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 





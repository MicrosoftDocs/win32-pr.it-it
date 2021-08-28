---
description: Ottiene il valore di pregio di un codec hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ffa9a962d9ed04b6a978da1534a6da4fa506e873d89d238bcbb2aa00fd865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847981"
---
# <a name="opm_get_codec_info"></a>OPM \_ GET \_ CODEC \_ INFO

Ottiene il valore di pregio di un codec hardware.



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------------|
| GUID richiesta | **OPM \_ GET \_ CODEC \_ INFO**                                                                 |
| Dati di input   | Struttura [**OPM \_ GET CODEC INFO \_ \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Restituisce i dati  | Struttura [**OPM \_ GET CODEC INFO \_ \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Commenti

Anche se questo comando usa [l'interfaccia OPM (Output Protection Manager),](output-protection-manager.md) si applica solo ai codificatori e decodificatori hardware. Non si applica ai dispositivi di output video.

In genere, è consigliabile non usare direttamente questo comando. Per ottenere il valore di pregio per un codec hardware, chiamare la [**funzione MFGetMFTMerit.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) Questa funzione esegue tutte le chiamate OPM necessarie per inviare il **comando OPM \_ GET CODEC \_ \_ INFO.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Richieste di stato OPM](opm-status-requests.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 





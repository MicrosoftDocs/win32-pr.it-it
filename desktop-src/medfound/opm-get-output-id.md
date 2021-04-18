---
description: Restituisce l'identificatore univoco del monitoraggio associato a questo output del video.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309057"
---
# <a name="opm_get_output_id"></a>\_ID di \_ output \_ Get di OPM

Restituisce l'identificatore univoco del monitoraggio associato a questo output del video.



| Requisito | Valore |
|--------------|------------------------------------------------------------------|
| GUID richiesta | \_ID di \_ output \_ Get di OPM                                             |
| Dati di input   | nessuno                                                             |
| Restituisce i dati  | Struttura [**\_ \_ \_ dei dati dell'ID di output di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) |



 

## <a name="remarks"></a>Commenti

Il driver video assegna un identificatore univoco a ogni monitoraggio. Questa query restituisce l'identificatore per il monitoraggio associato al puntatore [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Richieste di stato di OPM](opm-status-requests.md)
</dt> </dl>

 

 





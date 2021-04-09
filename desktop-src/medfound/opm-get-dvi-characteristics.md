---
description: Esegue una query se un connettore DVI (Digital Video Interface) supporta la versione DVI 1,1 o successiva.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049657"
---
# <a name="opm_get_dvi_characteristics"></a>\_caratteristiche di Get \_ DVI \_ per OPM

Esegue una query se un connettore DVI (Digital Video Interface) supporta la versione DVI 1,1 o successiva.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------|
| GUID richiesta | \_caratteristiche di Get \_ DVI \_ per OPM                                              |
| Dati di input   | nessuno                                                                        |
| Restituisce i dati  | Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Commenti

Se la query ha esito positivo, il membro **ulInformation** della struttura di [**\_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene uno dei valori seguenti.



| Valore                                     | Descrizione               |
|-------------------------------------------|---------------------------|
| Caratteristica di OPM \_ DVI \_ \_ 1 \_ 0            | Versione 1,0 di DVI.          |
| Caratteristiche di OPM \_ DVI \_ \_ 1 \_ 1 \_ o versione \_ successiva | DVI versione 1,1 o successiva. |



 

Questa query è supportata solo quando il tipo di connettore fisico è il tipo di connettore OPM \_ \_ \_ DVI. Per ottenere il tipo di connettore, inviare la query del [**\_ tipo di \_ connettore \_ OPM Get**](opm-get-connector-type.md) .

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

 

 





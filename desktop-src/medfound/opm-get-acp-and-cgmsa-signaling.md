---
description: 'Altre informazioni su: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309064"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>\_per la \_ \_ segnalazione di ACP e \_ CGMSA \_

Restituisce le informazioni seguenti su un output video:

-   Elenco di standard di protezione della televisione supportati dal driver.
-   Standard attualmente attivo.
-   Proporzioni correnti o altri dati di segnalazione.



| Requisito | Valore |
|--------------|-------------------------------------------------------------------------------------|
| GUID richiesta | \_per la \_ \_ segnalazione di ACP e \_ CGMSA \_                                                |
| Dati di input   | nessuno                                                                                |
| Restituisce i dati  | Struttura [**di \_ \_ \_ \_ segnalazione ACP e CGMSA di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Commenti

Questa query equivale alla \_ query DXVA COPPQuerySignaling utilizzata in Certified Output Protocol (Copp).

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

 

 





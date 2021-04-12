---
title: Funzioni di callback dell'applicazione client
description: Due tipi di firme di callback.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396586"
---
# <a name="client-application-callback-functions"></a>Funzioni di callback dell'applicazione client

Il Windows Biometric Framework supporta due tipi di firme di callback. A partire da Windows 8, il callback seguente è supportato. Si consiglia di implementare questo callback per tutte le nuove applicazioni. Questo callback, tuttavia, non può essere usato in Windows 7.



| Callback                                                                                     | Descrizione                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_callback di \_ completamento \_ asincrono PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Notifica all'applicazione client che un'operazione asincrona avviata tramite [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) o [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) è stata completata.<br/> |



 

Le funzioni di callback seguenti sono state introdotte in Windows 7. Si consiglia di non implementarli per le nuove applicazioni destinate a sistemi operativi Windows 8 e versioni successive.



| Callback                                                                                 | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_callback di acquisizione PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Restituisce i risultati della funzione asincrona [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .<br/> |
| [**\_callback di \_ acquisizione \_ registrazione PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Restituisce i risultati della funzione asincrona [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .<br/> |
| [**\_callback evento \_ PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Restituisce i risultati della funzione asincrona [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .<br/>           |
| [**\_callback di identificazione PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Restituisce i risultati della funzione asincrona [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .<br/>           |
| [**PWINBIO \_ individuare \_ il \_ callback del sensore**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Restituisce i risultati della funzione asincrona [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .<br/>   |
| [**PWINBIO \_ verifica \_ callback**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Restituisce i risultati della funzione asincrona [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .<br/>               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'applicazione client](client-application-reference.md)
</dt> </dl>

 

 






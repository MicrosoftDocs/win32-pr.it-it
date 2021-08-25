---
title: Funzioni di callback dell'applicazione client
description: Due tipi di firme di callback.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3e052df1821a5fd85bbba4ebbea3e6672d9e625b7d4258110fb19a5c234f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977101"
---
# <a name="client-application-callback-functions"></a>Funzioni di callback dell'applicazione client

Il Windows Biometric Framework supporta due tipi di firme di callback. A partire Windows 8, è supportato il callback seguente. È consigliabile implementare questo callback per tutte le nuove applicazioni. Questo callback non può tuttavia essere usato in Windows 7.



| Callback                                                                                     | Descrizione                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK DI COMPLETAMENTO \_ ASINCRONO PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Notifica all'applicazione client che un'operazione asincrona avviata tramite [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) o [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) è stata completata.<br/> |



 

Le funzioni di callback seguenti sono state introdotte nella Windows 7. È consigliabile non implementarli per le nuove applicazioni che hanno come destinazione Windows 8 sistemi operativi successivi.



| Callback                                                                                 | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK DI ACQUISIZIONE PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Restituisce i risultati della funzione [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) asincrona.<br/> |
| [**CALLBACK DI ACQUISIZIONE DI PWINBIO \_ \_ ENROLL \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Restituisce i risultati dalla funzione [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) asincrona.<br/> |
| [**CALLBACK DELL'EVENTO PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Restituisce i risultati della funzione [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) asincrona.<br/>           |
| [**CALLBACK DI IDENTIFICAZIONE PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Restituisce i risultati della [**funzione WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) asincrona.<br/>           |
| [**CALLBACK DEL SENSORE DI INDIVIDUAZIONE PWINBIO \_ \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Restituisce i risultati della [**funzione WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) asincrona.<br/>   |
| [**CALLBACK DI VERIFICA PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Restituisce i risultati della funzione [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) asincrona.<br/>               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento per l'applicazione client](client-application-reference.md)
</dt> </dl>

 

 






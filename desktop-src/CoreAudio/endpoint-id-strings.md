---
description: Stringhe di ID endpoint
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Stringhe di ID endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fdfbf12f3e037a23163bb3e8fef525db89c15904328c9e0fd8a71e5de004b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957310"
---
# <a name="endpoint-id-strings"></a>Stringhe di ID endpoint

In Windows Vista, il sistema genera stringhe di ID endpoint per identificare i [dispositivi endpoint audio](audio-endpoint-devices.md) nel sistema. Una stringa id endpoint è una stringa di caratteri wide con terminazione Null. La stringa dell'ID endpoint per un dispositivo endpoint audio specifico identifica in modo univoco il dispositivo tra tutti i dispositivi endpoint audio nel sistema.

Se un sistema contiene due o più dispositivi adattatore audio identici, i dispositivi endpoint audio corrispondenti avranno nomi descrittivi identici, ma ogni dispositivo endpoint avrà una stringa id endpoint univoca. Per altre informazioni su come ottenere il nome descrittivo di un dispositivo endpoint, vedere [Proprietà del dispositivo](device-properties.md).

Dopo aver ottenuto [**un'istanza dell'interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) per un dispositivo endpoint audio, un client può chiamare il metodo [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere la stringa dell'ID endpoint per il dispositivo. Un client può usare la stringa dell'ID endpoint per creare un'istanza del dispositivo endpoint audio in un secondo momento o in un processo diverso chiamando il [**metodo IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)

Un client può disporre di ricevere una notifica quando lo stato di qualsiasi dispositivo endpoint audio cambia. Per ricevere notifiche, il client implementa [**un'interfaccia IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registra tale interfaccia con l'API MMDevice. Quando lo stato di un dispositivo endpoint cambia, l'API MMDevice chiama il metodo appropriato nell'interfaccia [**EDataFlow del**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) client. Uno dei parametri di input per il metodo è la stringa dell'ID endpoint che identifica il dispositivo endpoint il cui stato è stato modificato. Per altre informazioni su **EDataFlow,** vedere [Eventi dispositivo](device-events.md).

Le API audio legacy, ad esempio DirectSound e le Windows multimediali, dispongono di interfacce personalizzate per l'enumerazione e l'identificazione dei dispositivi audio. In Windows Vista queste interfacce sono state estese per fornire le stringhe di ID endpoint che identificano i dispositivi endpoint alla base delle astrazioni dei dispositivi presentate dalle API.

Durante l'enumerazione del dispositivo DirectSound, DirectSound fornisce la stringa dell'ID endpoint per ogni dispositivo enumerato. Per altre informazioni, vedere [Eventi audio per applicazioni audio legacy.](audio-events-for-legacy-audio-applications.md)

Per ottenere la stringa dell'ID endpoint per un dispositivo waveform legacy, usare la funzione [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) o [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) per inviare un messaggio DRV QUERYFUNCTIONINSTANCEID al driver del dispositivo \_ waveform. Per un esempio di codice che illustra l'uso di questo messaggio, vedere Ruoli del dispositivo per applicazioni [Windows multimediali](device-roles-for-legacy-windows-multimedia-applications.md).

Per altre informazioni sull'uso delle funzionalità delle API audio di base per migliorare le applicazioni che usano API audio legacy, vedere Interoperabilità con le API [audio legacy.](interoperability-with-legacy-audio-apis.md)

I client devono considerare il contenuto della stringa dell'ID endpoint come opaco. In altre informazioni, i client non devono tentare di analizzare il contenuto della stringa per ottenere informazioni sul dispositivo. Il motivo è che il formato della stringa non è definito e potrebbe cambiare da un'implementazione del modulo di sistema dell'API MMDevice a quella successiva.

La durata di una stringa di ID endpoint è associata all'installazione del dispositivo. La stringa dell'ID endpoint di un dispositivo cambia se l'utente aggiorna il driver di dispositivo o se l'utente disinstalla il dispositivo e lo installa di nuovo. Tuttavia, la stringa dell'ID endpoint rimane invariata tra i riavvii del sistema e la stringa dell'ID endpoint di un dispositivo audio USB rimane invariata se l'utente scollega il dispositivo e lo collega nuovamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 

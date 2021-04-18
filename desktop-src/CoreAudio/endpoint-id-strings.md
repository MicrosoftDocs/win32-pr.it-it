---
description: Stringhe ID endpoint
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Stringhe ID endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04c07da78b92795ebadd7d8f9731f7188ae8dc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304422"
---
# <a name="endpoint-id-strings"></a>Stringhe ID endpoint

In Windows Vista, il sistema genera stringhe ID endpoint per identificare i [dispositivi dell'endpoint audio](audio-endpoint-devices.md) nel sistema. Una stringa ID endpoint è una stringa di caratteri wide con terminazione null. La stringa dell'ID endpoint per un determinato dispositivo dell'endpoint audio identifica in modo univoco il dispositivo tra tutti i dispositivi dell'endpoint audio nel sistema.

Se un sistema contiene due o più dispositivi scheda audio identici, i dispositivi endpoint audio corrispondenti avranno nomi descrittivi identici, ma ogni dispositivo dell'endpoint avrà una stringa ID univoco. Per ulteriori informazioni su come ottenere il nome descrittivo di un dispositivo endpoint, vedere [proprietà del dispositivo](device-properties.md).

Dopo aver ottenuto un'istanza dell'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) per un dispositivo endpoint audio, un client può chiamare il metodo [**IMMDevice:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere la stringa dell'ID endpoint per il dispositivo. Un client può usare la stringa dell'ID endpoint per creare un'istanza del dispositivo dell'endpoint audio in un secondo momento o in un processo diverso chiamando il metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .

Un client può disporre di ricevere una notifica quando viene modificato lo stato di qualsiasi dispositivo dell'endpoint audio. Per ricevere le notifiche, il client implementa un'interfaccia [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registra tale interfaccia con l'API MMDevice. Quando viene modificato lo stato di un dispositivo dell'endpoint, l'API MMDevice chiama il metodo appropriato nell'interfaccia [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) del client. Uno dei parametri di input per il metodo è la stringa dell'ID endpoint che identifica il dispositivo dell'endpoint il cui stato è stato modificato. Per ulteriori informazioni su **EDataFlow**, vedere la pagina relativa [agli eventi del dispositivo](device-events.md).

Le API audio legacy, ad esempio DirectSound e le funzioni multimediali di Windows, hanno interfacce proprie per l'enumerazione e l'identificazione di dispositivi audio. In Windows Vista queste interfacce sono state estese per fornire le stringhe ID endpoint che identificano i dispositivi endpoint sottostanti alle astrazioni dei dispositivi presentate dalle API.

Durante l'enumerazione del dispositivo DirectSound, DirectSound fornisce la stringa dell'ID endpoint per ogni dispositivo enumerato. Per altre informazioni, vedere [eventi audio per le applicazioni audio legacy](audio-events-for-legacy-audio-applications.md).

Per ottenere la stringa dell'ID endpoint per un dispositivo di forma d'onda legacy, usare la funzione [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) o [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) per inviare un \_ messaggio DRV QUERYFUNCTIONINSTANCEID al driver di dispositivo waveform. Per un esempio di codice che illustra l'uso di questo messaggio, vedere [ruoli del dispositivo per le applicazioni Windows multimediali legacy](device-roles-for-legacy-windows-multimedia-applications.md).

Per altre informazioni sull'uso delle funzionalità delle API audio principali per migliorare le applicazioni che usano le API audio legacy, vedere [interoperabilità con le API audio legacy](interoperability-with-legacy-audio-apis.md).

I client devono trattare il contenuto della stringa dell'ID dell'endpoint come opaco. Ovvero i client non devono tentare di analizzare il contenuto della stringa per ottenere informazioni sul dispositivo. Il motivo è che il formato della stringa non è definito e può cambiare da un'implementazione del modulo del sistema API MMDevice al successivo.

Il ciclo di vita di una stringa ID endpoint è associato all'installazione del dispositivo. La stringa dell'ID endpoint di un dispositivo cambia se l'utente aggiorna il driver di dispositivo o se l'utente disinstalla il dispositivo e lo installa nuovamente. Tuttavia, la stringa dell'ID endpoint rimane invariata tra i riavvii del sistema e la stringa ID endpoint di un dispositivo audio USB rimane invariata se l'utente scollega il dispositivo e lo collega di nuovo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 

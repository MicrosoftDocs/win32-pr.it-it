---
description: Enumerazione dei dispositivi audio
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Enumerazione dei dispositivi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707b9a88181c83344757c711af1c0199c19ebc16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049211"
---
# <a name="enumerating-audio-devices"></a>Enumerazione dei dispositivi audio

La prima attività di un'applicazione audio client è trovare un dispositivo audio adatto da usare. L' [API MMDevice](mmdevice-api.md) consente ai client di individuare i [dispositivi dell'endpoint audio](audio-endpoint-devices.md) nel sistema e di determinare quali dispositivi sono appropriati per l'uso da parte dell'applicazione. Questa API consente ai client di recuperare le raccolte dei dispositivi endpoint disponibili e di ottenere le funzionalità di ogni dispositivo. Il file di intestazione mmdeviceapi. h definisce le interfacce nell'API MMDevice.

Una scheda audio potrebbe contenere diversi dispositivi, ad esempio un dispositivo di rendering Wave e un dispositivo di acquisizione Wave. Si tratta di dispositivi adapter anziché di dispositivi endpoint. Come indicato in precedenza, i dispositivi dell'adapter vengono registrati dal gestore Plug and Play, a differenza dei dispositivi endpoint, che vengono registrati da Gestione endpoint. Ogni dispositivo adapter supporta in genere uno o più dispositivi endpoint. Un dispositivo dell'endpoint di rendering (ad esempio, cuffie) può ricevere un flusso di dati audio da un'applicazione client e un dispositivo dell'endpoint di acquisizione, ad esempio un microfono, può inviare un flusso audio a un'applicazione client.

Prima di enumerare i dispositivi endpoint nel sistema, il client deve prima chiamare la funzione Windows [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un enumeratore di dispositivo. Un enumeratore di dispositivo è un oggetto con un'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Per informazioni su **CoCreateInstance**, vedere la documentazione Windows SDK.

Il client chiama il metodo [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) per creare una raccolta di oggetti endpoint. Ogni oggetto endpoint rappresenta un dispositivo endpoint audio nel sistema. In questa chiamata il client specifica se la raccolta deve contenere tutti i dispositivi di rendering del sistema, tutti i dispositivi di acquisizione o entrambi.

Una raccolta di dispositivi è un oggetto con un'interfaccia [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . Ogni elemento in una raccolta di dispositivi è un oggetto endpoint con almeno le due interfacce seguenti:

-   Interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . Un client ottiene un riferimento all'interfaccia **IMMDevice** di un oggetto endpoint in una raccolta di dispositivi chiamando il metodo [**IMMDeviceCollection:: Item**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item) .
-   Interfaccia [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) . Un client ottiene un riferimento all'interfaccia **IMMEndpoint** di un oggetto endpoint chiamando il metodo [**IMMDevice:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

Dopo il recupero di una raccolta di dispositivi endpoint, il client può eseguire una query sulle proprietà dei singoli dispositivi nella raccolta per determinarne l'idoneità per l'utilizzo. Per un esempio di codice che illustra come enumerare i dispositivi endpoint ed eseguire query sulle relative proprietà, vedere [proprietà del dispositivo](device-properties.md).

Dopo aver selezionato un dispositivo appropriato, il client può chiamare il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per attivare le interfacce specifiche del dispositivo in [WASAPI](wasapi.md), l' [API DeviceTopology](devicetopology-api.md)e l' [API EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 

---
description: Enumerazione di dispositivi audio
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Enumerazione di dispositivi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5d21ec2de2b08ca3c6f26884bd210b2f149caaa9e3b6a4402b69dde9fb7540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018379"
---
# <a name="enumerating-audio-devices"></a>Enumerazione di dispositivi audio

La prima attività di un'applicazione audio client è trovare un dispositivo audio appropriato da usare. [L'API MMDevice](mmdevice-api.md) consente ai client di individuare [i dispositivi endpoint audio](audio-endpoint-devices.md) nel sistema e determinare quali dispositivi sono adatti all'uso da parte dell'applicazione. Questa API consente ai client di recuperare le raccolte dei dispositivi endpoint disponibili e di ottenere le funzionalità di ogni dispositivo. Il file di intestazione Mmdeviceapi.h definisce le interfacce nell'API MMDevice.

Un adattatore audio può contenere diversi dispositivi, ad esempio un dispositivo di rendering delle onde e un dispositivo di acquisizione d'onda. Si tratta di dispositivi adapter anziché di dispositivi endpoint. Come accennato in precedenza, i dispositivi adapter vengono registrati da Plug and Play Manager, a differenza dei dispositivi endpoint, registrati da Gestione endpoint. Ogni dispositivo adattatore supporta in genere uno o più dispositivi endpoint. Un dispositivo endpoint di rendering (ad esempio, le cuffi) può ricevere un flusso di dati audio da un'applicazione client e un dispositivo endpoint di acquisizione (ad esempio, un microfono) può inviare un flusso audio a un'applicazione client.

Prima di enumerare i dispositivi endpoint nel sistema, il client deve chiamare la funzione [**Windows CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un enumeratore dispositivo. Un enumeratore di dispositivo è un oggetto con [**un'interfaccia IMMDeviceEnumerator.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Per informazioni su **CoCreateInstance,** vedere la documentazione Windows SDK.

Il client chiama il [**metodo IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) per creare una raccolta di oggetti endpoint. Ogni oggetto endpoint rappresenta un dispositivo endpoint audio nel sistema. In questa chiamata, il client specifica se la raccolta deve contenere tutti i dispositivi di rendering nel sistema, tutti i dispositivi di acquisizione o entrambi.

Una raccolta di dispositivi è un oggetto con [**un'interfaccia IMMDeviceCollection.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) Ogni elemento in una raccolta di dispositivi è un oggetto endpoint con almeno le due interfacce seguenti:

-   Interfaccia [**IMMDevice.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) Un client ottiene un riferimento **all'interfaccia IMMDevice** di un oggetto endpoint in una raccolta di dispositivi chiamando il [**metodo IMMDeviceCollection::Item.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item)
-   Interfaccia [**IMMEndpoint.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) Un client ottiene un riferimento **all'interfaccia IMMEndpoint** di un oggetto endpoint chiamando il [**metodo IMMDevice::QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

Dopo il recupero di una raccolta di dispositivi endpoint, il client può eseguire una query sulle proprietà dei singoli dispositivi nella raccolta per determinarne l'idoneità all'uso. Per un esempio di codice che illustra come enumerare i dispositivi endpoint ed eseguire query sulle relative proprietà, vedere [Proprietà del dispositivo.](device-properties.md)

Dopo aver selezionato un dispositivo appropriato, il client può chiamare il metodo [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per attivare le interfacce specifiche del dispositivo in [WASAPI,](wasapi.md)l'API [DeviceTopology](devicetopology-api.md)e l'API [EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 

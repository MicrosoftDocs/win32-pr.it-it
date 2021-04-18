---
title: Implementazione di un enumeratore di endpoint audio personalizzato
description: A partire da Windows Server 2008 R2, è possibile implementare un enumeratore endpoint audio remoto personalizzato come parte di un provider di protocollo Desktop remoto.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300590"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implementazione di un enumeratore di endpoint audio personalizzato

A partire da Windows Server 2008 R2, è possibile implementare un enumeratore endpoint audio remoto personalizzato come parte di un provider di protocollo Desktop remoto. Un provider di protocollo Desktop remoto può usare un enumeratore di endpoint audio personalizzato per recuperare una raccolta di endpoint audio con un set specifico di funzionalità.

**Per implementare un enumeratore di endpoint audio remoto personalizzato**

1.  La soluzione di enumeratore endpoint personalizzato deve implementare quattro tipi principali di oggetti: oggetti enumeratore dispositivi, oggetti raccolta dispositivi, oggetti dispositivo e oggetti archivio proprietà.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Tipo di oggetto</th>
    <th>Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Oggetto enumeratore dispositivi<br/></td>
    <td>Un oggetto enumeratore di dispositivi fornisce la funzionalità di enumeratore dell'endpoint. Espone metodi che restituiscono un endpoint predefinito e raccolte di endpoint specificati. Ad esempio, a seconda dei criteri specificati, l'enumeratore può restituire gli endpoint di comunicazione, gli endpoint di riproduzione o gli endpoint di acquisizione. L'oggetto enumeratore Device deve implementare l'interfaccia <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Oggetto raccolta dispositivi<br/></td>
    <td>Un oggetto raccolta dispositivi rappresenta una raccolta di dispositivi audio. Deve implementare l'interfaccia <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> .<br/></td>
    </tr>
    <tr class="odd">
    <td>Oggetto dispositivo<br/></td>
    <td>Un oggetto dispositivo rappresenta un dispositivo audio particolare. Consente di accedere all'archivio delle proprietà del dispositivo audio ed espone le interfacce di riproduzione e acquisizione audio disponibili sul dispositivo. L'oggetto dispositivo deve implementare le interfacce <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> e <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Oggetto archivio proprietà<br/></td>
    <td>Un oggetto archivio proprietà espone le proprietà associate a un dispositivo audio. Alcune di queste proprietà vengono usate dal sistema, ma le applicazioni possono archiviare anche proprietà arbitrarie con l'endpoint audio.<br/> Tutti i dispositivi audio hanno le tre proprietà seguenti:<br/>
    <ul>
    <li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li>
    </ul>
L'oggetto archivio proprietà deve implementare l'interfaccia <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> .<br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  L'enumeratore endpoint personalizzato deve essere implementato in una DLL che può essere caricata nel sistema audio e in altre applicazioni. La DLL deve essere firmata in modo che i processi protetti possano caricarla. La DLL deve implementare ed esportare la funzione [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) , che funge da punto di ingresso all'enumeratore dell'endpoint personalizzato.

Il servizio Servizi Desktop remoto chiama il metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) e imposta il parametro *QueryType* su **WTS \_ query \_ AUDIOENUM \_ dll** per recuperare il nome dell'oggetto enumeratore.

Gli oggetti enumeratore personalizzati utilizzano interfacce simili a COM e un meccanismo di conteggio dei riferimenti simile a COM, ma non sono veri oggetti COM. L'enumeratore di endpoint personalizzato deve avere la possibilità di utilizzare interfacce audio legacy utilizzate da applicazioni che non supportano COM. Per questo motivo, l'enumeratore endpoint personalizzato non deve basarsi sul meccanismo di gestione del ciclo di vita di COM. I consumer dell'enumeratore dell'endpoint audio, ad esempio MMDevAPI.dll, caricano la DLL dell'enumeratore di endpoint personalizzato quando richiesto dalle applicazioni utente e non scaricano l'enumeratore mentre l'enumeratore include un riferimento a un oggetto enumeratore di dispositivi, oggetto della raccolta dispositivi, oggetto dispositivo o oggetto archivio proprietà. Tuttavia, non è possibile per questi consumer tenere traccia dei riferimenti ad altri tipi di oggetti di proprietà dell'enumeratore di endpoint personalizzato. Di conseguenza, è consigliabile che l'enumeratore dell'endpoint personalizzato non crei oggetti che potrebbero sopravvivere a questi quattro tipi di oggetti.

## <a name="to-implement-a-custom-audio-endpoint"></a>Per implementare un endpoint audio personalizzato

Per implementare un enumeratore di dispositivo audio personalizzato, è necessario implementare un endpoint audio personalizzato. Il modo in cui i dispositivi audio personalizzati sono collegati consiste nell'usare le due istruzioni seguenti:

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

Non si prevede di implementare l'elenco completo delle interfacce [**IMMDevice:: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) nell'enumeratore dispositivo audio personalizzato. In alternativa, è necessario implementare [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) e [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Facoltativamente, è possibile implementare altri, ad esempio [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume). Per qualsiasi interfaccia non implementata, è necessario restituire **E \_ nointerface** (è necessario usare questo codice di errore specifico). Windows eseguirà quindi il fallback a un'implementazione predefinita dell'interfaccia (ad esempio, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).

Per la documentazione di riferimento aggiuntiva su come implementare e registrare gli endpoint audio, vedere [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Per un diagramma che illustra il funzionamento di WASAPI, vedere [componenti audio in modalità utente](/windows/desktop/CoreAudio/user-mode-audio-components). Si noti che tutte le audio in modalità utente sono nuove a partire da Windows Server 2008.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di Remote Desktop Protocol](creating-a-custom-remote-protocol.md)
</dt> <dt>

[**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[**IMMDevice**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDeviceCollection**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMEndpoint**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>
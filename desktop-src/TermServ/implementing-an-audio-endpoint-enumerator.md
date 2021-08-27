---
title: Implementazione di un enumeratore di endpoint audio personalizzato
description: A partire Windows Server 2008 R2, è possibile implementare un enumeratore di endpoint audio remoto personalizzato come parte di un provider Desktop remoto protocol.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae135d19e13e3b78fddbdd58bccd476b7e5ee7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478857"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implementazione di un enumeratore di endpoint audio personalizzato

A partire Windows Server 2008 R2, è possibile implementare un enumeratore di endpoint audio remoto personalizzato come parte di un provider Desktop remoto protocol. Un provider Desktop remoto protocollo può usare un enumeratore di endpoint audio personalizzato per recuperare una raccolta di endpoint audio con un set specifico di funzionalità.

**Per implementare un enumeratore di endpoint audio remoto personalizzato**

1.  La soluzione di enumeratore dell'endpoint personalizzato deve implementare quattro tipi principali di oggetti: oggetti enumeratore dispositivo, oggetti raccolta dispositivi, oggetti dispositivo e oggetti archivio proprietà.

    

    
| Tipo di oggetto | Descrizione | 
|-------------|-------------|
| Oggetto enumeratore dispositivo<br /> | Un oggetto enumeratore dispositivo fornisce la funzionalità di enumeratore dell'endpoint. Espone metodi che restituiscono un endpoint predefinito e raccolte di endpoint specificate. A seconda dei criteri specificati, ad esempio, l'enumeratore può restituire endpoint di comunicazione, endpoint di riproduzione o endpoint di acquisizione. L'oggetto enumeratore dispositivo deve implementare <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>l'interfaccia IMMDeviceEnumerator.</strong></a><br /> | 
| Oggetto raccolta dispositivi<br /> | Un oggetto raccolta di dispositivi rappresenta una raccolta di dispositivi audio. Deve implementare <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>l'interfaccia IMMDeviceCollection.</strong></a><br /> | 
| Oggetto dispositivo<br /> | Un oggetto dispositivo rappresenta un particolare dispositivo audio. Fornisce l'accesso all'archivio delle proprietà del dispositivo audio ed espone le interfacce di riproduzione e acquisizione audio disponibili nel dispositivo. L'oggetto dispositivo deve implementare <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>le interfacce IMMDevice</strong></a> <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>e IMMEndpoint.</strong></a><br /> | 
| Oggetto archivio delle proprietà<br /> | Un oggetto archivio proprietà espone le proprietà associate a un dispositivo audio. Alcune di queste proprietà vengono usate dal sistema, ma le applicazioni possono archiviare proprietà arbitrarie anche con l'endpoint audio.<br /> Tutti i dispositivi audio hanno le tre proprietà seguenti:<br /><ul><li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li></ul>    L'oggetto archivio delle proprietà deve implementare <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">l'interfaccia IPropertyStore.</a><br /> | 


    

     

2.  L'enumeratore dell'endpoint personalizzato deve essere implementato in una DLL che può essere caricata nel sistema audio e in altre applicazioni. La DLL deve essere firmata in modo che i processi protetti possano caricarla. La DLL deve implementare ed esportare la [**funzione GetTSAudioEndpointEnumeratorForSession,**](gettsaudioendpointenumeratorforsession.md) che funge da punto di ingresso all'enumeratore dell'endpoint personalizzato.

Il Servizi Desktop remoto chiama il [**metodo QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) e imposta il parametro *QueryType* su **WTS \_ DLL QUERY \_ AUDIOENUM \_** per recuperare il nome dell'oggetto enumeratore.

Gli oggetti enumeratore personalizzati usano interfacce di tipo COM e un meccanismo di conteggio dei riferimenti simile a COM, ma non sono oggetti COM veri. L'enumeratore dell'endpoint personalizzato deve essere in grado di usare interfacce audio legacy utilizzate da applicazioni che non supportano COM. Per questo motivo, l'enumeratore dell'endpoint personalizzato non deve basarsi sul meccanismo di gestione del ciclo di vita DI COM. I consumer dell'enumeratore dell'endpoint audio, ad esempio MMDevAPI.dll, caricano la DLL dell'enumeratore dell'endpoint personalizzato quando richiesto dalle applicazioni utente e non scaricano l'enumeratore mentre l'enumeratore contiene un riferimento a un oggetto enumeratore dispositivo, un oggetto raccolta dispositivi, un oggetto dispositivo o un oggetto archivio proprietà. Non è tuttavia possibile per questi consumer tenere traccia dei riferimenti ad altri tipi di oggetti di proprietà dell'enumeratore dell'endpoint personalizzato. Di conseguenza, è consigliabile che l'enumeratore dell'endpoint personalizzato non crei oggetti che potrebbero avere una durata superiore a questi quattro tipi di oggetti.

## <a name="to-implement-a-custom-audio-endpoint"></a>Per implementare un endpoint audio personalizzato

Per implementare un enumeratore di dispositivo audio personalizzato, è necessario implementare un endpoint audio personalizzato. Il modo in cui i dispositivi audio personalizzati vengono collegati è tramite le due istruzioni seguenti:

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

Non è previsto che l'utente implementi l'elenco completo delle [**interfacce IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) nell'enumeratore del dispositivo audio personalizzato. È invece necessario implementare [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) e [**IAudioInputEndpointRT.**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) Facoltativamente, è possibile implementarne altre, ad [**esempio IAudioEndpointVolume.**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume) Per qualsiasi interfaccia non implementata, è necessario restituire **E \_ NOINTERFACE** (è necessario usare questo codice di errore specifico). Windows verrà quindi riportato a un'implementazione predefinita dell'interfaccia (ad [**esempio, IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).

Per documentazione di riferimento aggiuntiva su come implementare e registrare endpoint audio, vedere [**IAudioInputEndpointRT.**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) Per un diagramma che illustra il funzionamento di WASAPI, vedere [Componenti audio in modalità utente.](/windows/desktop/CoreAudio/user-mode-audio-components) Si noti che tutto l'audio in modalità utente è una novità a partire Windows Server 2008.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider Remote Desktop Protocol](creating-a-custom-remote-protocol.md)
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

[Ipropertystore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>

---
description: Topologie del dispositivo
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Topologie del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524257"
---
# <a name="device-topologies"></a>Topologie del dispositivo

L' [API DeviceTopology](devicetopology-api.md) fornisce ai client il controllo su un'ampia gamma di funzioni interne di schede audio a cui non possono accedere tramite l'API [MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)o l' [API EndpointVolume](endpointvolume-api.md).

Come spiegato in precedenza, l' [API MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)e l' [API EndpointVolume](endpointvolume-api.md) presentano microfoni, altoparlanti, cuffie e altri dispositivi di input e output audio ai client come [dispositivi di endpoint audio](audio-endpoint-devices.md). Il modello di dispositivo endpoint fornisce ai client un comodo accesso ai controlli volume e mute nei dispositivi audio. I client che richiedono solo questi controlli semplici possono evitare di attraversare le topologie interne dei dispositivi hardware nelle schede audio.

In Windows Vista, il motore audio configura automaticamente le topologie dei dispositivi audio per l'uso da parte delle applicazioni audio. Quindi, raramente, le applicazioni devono usare l'API DeviceTopology per questo scopo. Si supponga, ad esempio, che una scheda audio includa un multiplexer di input in grado di acquisire un flusso da un input di riga o un microfono, ma che non sia in grado di acquisire flussi da entrambi i dispositivi endpoint nello stesso momento. Si supponga che l'utente abbia abilitato le applicazioni in modalità esclusiva per precedere l'uso di un dispositivo endpoint audio dalle applicazioni in modalità condivisa, come descritto in [flussi in modalità esclusiva](exclusive-mode-streams.md). Se un'applicazione in modalità condivisa sta registrando un flusso dall'input di riga nel momento in cui un'applicazione in modalità esclusiva inizia a registrare un flusso dal microfono, il motore audio passa automaticamente il multiplexer dall'input di riga al microfono. Al contrario, nelle versioni precedenti di Windows, incluso Windows XP, l'applicazione in modalità esclusiva in questo esempio utilizzerebbe le funzioni **mixerXxx** nell'API multimediale di Windows per attraversare le topologie dei dispositivi dell'adapter, individuare il multiplexer e configurare multiplexer per selezionare l'input del microfono. In Windows Vista questi passaggi non sono più necessari.

Tuttavia, alcuni client potrebbero richiedere il controllo esplicito dei tipi di controlli hardware audio a cui non è possibile accedere tramite l'API MMDevice, WASAPI o l'API EndpointVolume. Per questi client, l'API DeviceTopology consente di attraversare le topologie dei dispositivi Adapter per individuare e gestire i controlli audio nei dispositivi. Le applicazioni che usano l'API di DeviceTopology devono essere progettate con attenzione per evitare di interferire con i criteri audio di Windows e le configurazioni interne dei dispositivi audio condivisi con altre applicazioni. Per ulteriori informazioni sui criteri audio di Windows, vedere [componenti audio in modalità utente](user-mode-audio-components.md).

L'API DeviceTopology fornisce interfacce per l'individuazione e la gestione dei seguenti tipi di controlli audio in una topologia di dispositivo:

-   Controllo di guadagno automatico
-   Controllo Bass
-   Selettore input (Multiplexer)
-   Controllo della sonorità
-   Controllo midrange
-   Disattiva controllo
-   Selettore di output (demultiplexer)
-   Misurazione picco
-   Controllo Treble
-   Controllo volume

Inoltre, l'API DeviceTopology consente ai client di eseguire query sui dispositivi Adapter per ottenere informazioni sui formati di flusso supportati. Il file di intestazione Devicetopology. h definisce le interfacce nell'API DeviceTopology.

Nel diagramma seguente viene illustrato un esempio di diverse topologie di dispositivo connesse per la parte di una scheda PCI che acquisisce l'audio da un microfono, un input di linea e un lettore di CD.

![esempio di quattro topologie di dispositivi connessi](images/fig2.jpg)

Il diagramma precedente Mostra i percorsi dati che portano dagli input analoghi al bus di sistema. Ognuno dei dispositivi seguenti è rappresentato come un oggetto topologia di dispositivo con un'interfaccia [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :

-   Dispositivo di acquisizione Wave
-   Dispositivo multiplexer di input
-   Dispositivo endpoint A
-   Dispositivo endpoint B

Si noti che il diagramma della topologia combina i dispositivi Adapter (i dispositivi Wave Capture e input multiplexer) con i dispositivi endpoint. Attraverso le connessioni tra i dispositivi, i dati audio passano da un dispositivo a quello successivo. Su ogni lato di una connessione è presente un connettore (con etichetta con nel diagramma) tramite il quale i dati entrano o lasciano un dispositivo.

Sul lato sinistro del diagramma, i segnali provenienti dai jack di input della riga e del microfono immettono i dispositivi endpoint.

All'interno del dispositivo di acquisizione Wave e il dispositivo multiplexer di input sono funzioni di elaborazione del flusso, che, nella terminologia dell'API DeviceTopology, sono denominate unità secondarie. Nel diagramma precedente vengono visualizzati i tipi di unità secondari seguenti:

-   Controllo volume (con etichetta VOL)
-   Controllo mute (con etichetta mute)
-   Multiplexer (o selettore input; con etichetta MUX)
-   Convertitore analogico-digitale (ADC con etichetta)

Le impostazioni nelle unità secondarie volume, mute e multiplexer possono essere controllate dai client e l'API DeviceTopology fornisce le interfacce di controllo ai client per controllarle. In questo esempio, la sottounità ADC non ha impostazioni di controllo. Di conseguenza, l'API DeviceTopology non fornisce alcuna interfaccia di controllo per ADC.

Nella terminologia dell'API DeviceTopology, i connettori e le unità secondarie appartengono alla stessa categoria generale, parti. Tutte le parti, indipendentemente dal fatto che si tratti di connettori o unità secondarie, forniscono un set comune di funzioni. L'API DeviceTopology implementa un'interfaccia [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) per rappresentare le funzioni generiche comuni ai connettori e alle sottounità. L'API implementa le interfacce [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) e [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) per rappresentare gli aspetti specifici dei connettori e delle sottounità.

L'API DeviceTopology costruisce le topologie del dispositivo di acquisizione Wave e del dispositivo multiplexer di input dai filtri di streaming kernel (KS) che il driver audio espone al sistema operativo per rappresentare questi dispositivi. Il driver della scheda audio implementa le interfacce **IMiniportWaveXxx** e **IMiniportTopology** per rappresentare le parti dipendenti dall'hardware di questi filtri. per ulteriori informazioni su queste interfacce e sui filtri KS, vedere la documentazione di Windows DDK.

L'API DeviceTopology costruisce topologie semplici per rappresentare i dispositivi endpoint a e B nel diagramma precedente. La topologia del dispositivo di un endpoint è costituita da un singolo connettore. Questa topologia è semplicemente un segnaposto per il dispositivo endpoint e non contiene unità secondarie per l'elaborazione dei dati audio. Infatti, i dispositivi Adapter contengono tutte le sottounità usate dalle applicazioni client per controllare l'elaborazione audio. La topologia del dispositivo di un endpoint viene utilizzata principalmente come punto di partenza per l'esplorazione delle topologie dei dispositivi adapter.

Le connessioni interne tra due parti di una topologia di dispositivo sono denominate collegamenti. L'API DeviceTopology fornisce metodi per attraversare i collegamenti da una parte all'altra in una topologia di dispositivo. L'API fornisce anche metodi per attraversare le connessioni tra topologie di dispositivi.

Per iniziare l'esplorazione di un set di topologie di dispositivi connessi, un'applicazione client attiva l'interfaccia **IDeviceTopology** di un dispositivo endpoint audio. Il connettore in un dispositivo endpoint si connette a un connettore in una scheda audio o a una rete. Se l'endpoint si connette a un dispositivo in una scheda audio, i metodi nell'API DeviceTopology consentono all'applicazione di eseguire l'istruzione attraverso la connessione dall'endpoint alla scheda ottenendo un riferimento all'interfaccia **IDeviceTopology** del dispositivo adattatore sull'altro lato della connessione. Una rete, d'altra parte, non ha una topologia del dispositivo. Una connessione di rete invia tramite pipe un flusso audio a un client che accede al sistema in modalità remota.

L'API DeviceTopology consente di accedere solo alle topologie dei dispositivi hardware in una scheda audio. I dispositivi esterni sul bordo sinistro del diagramma e i componenti software sul bordo destro esulano dall'ambito dell'API. Le linee tratteggiate su entrambi i lati del diagramma rappresentano i limiti dell'API DeviceTopology. Il client può usare l'API per esplorare un percorso dati che si estende dal jack di input al bus di sistema, ma l'API non può penetrare oltre questi limiti.

A ogni connettore del diagramma precedente è associato un tipo di connessione che indica il tipo di connessione eseguita dal connettore. Pertanto, i connettori sui due lati di una connessione hanno sempre tipi di connessione identici. Il tipo di connessione è indicato da un valore di enumerazione [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) : fisico \_ esterno, fisico \_ interno, software \_ fisso, i/ \_ o software o rete. Le connessioni tra il dispositivo multiplexer di input e i dispositivi endpoint A e B sono di tipo \_ External fisico, il che significa che la connessione rappresenta una connessione fisica a un dispositivo esterno (in altre parole, un jack audio accessibile dall'utente). La connessione al segnale analogico dal lettore CD interno è di tipo \_ Internal fisico, che indica una connessione fisica a un dispositivo ausiliario installato all'interno dello chassis del sistema. La connessione tra il dispositivo di acquisizione Wave e il dispositivo multiplexer di input è di tipo software \_ fixed, che indica una connessione permanente che è fissa e non può essere configurata in controllo software. Infine, la connessione al bus di sistema sul lato destro del diagramma è di tipo software \_ io, che indica che l'i/O dei dati per la connessione viene implementato da un motore DMA sotto controllo software. Il diagramma non include un esempio di tipo di connessione di rete.

Il client inizia a attraversare un percorso dati sul dispositivo endpoint. In primo luogo, il client ottiene un'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) che rappresenta il dispositivo dell'endpoint, come illustrato in [enumerazione dei dispositivi audio](enumerating-audio-devices.md). Per ottenere l'interfaccia **IDeviceTopology** per il dispositivo endpoint, il client chiama il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *IID* impostato su REFIID IID \_ IDeviceTopology.

Nell'esempio del diagramma precedente, il dispositivo multiplexer di input contiene tutti i controlli hardware (volume, mute e multiplexer) per i flussi di acquisizione dai jack di input di riga e microfono. Nell'esempio di codice seguente viene illustrato come ottenere l'interfaccia **IDeviceTopology** per il dispositivo multiplexer di input dall'interfaccia **IMMDevice** per il dispositivo endpoint per l'input o il microfono della riga:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



La funzione GetHardwareDeviceTopology nell'esempio di codice precedente esegue i passaggi seguenti per ottenere l'interfaccia **IDeviceTopology** per il dispositivo multiplexer di input:

1.  Chiamare il metodo **IMMDevice:: Activate** per ottenere l'interfaccia **IDeviceTopology** per il dispositivo endpoint.
2.  Con l'interfaccia **IDeviceTopology** ottenuta nel passaggio precedente, chiamare il metodo [**IDeviceTopology:: GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) per ottenere l'interfaccia **IConnector** del connettore singolo (numero di connettore 0) nel dispositivo dell'endpoint.
3.  Con l'interfaccia **IConnector** ottenuta nel passaggio precedente, chiamare il metodo [**IConnector:: GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) per ottenere l'interfaccia **IConnector** del connettore nel dispositivo multiplexer di input.
4.  Eseguire una query sull'interfaccia **IConnector** ottenuta nel passaggio precedente per la relativa interfaccia **IPart** .
5.  Con l'interfaccia **IPart** ottenuta nel passaggio precedente, chiamare il metodo [**IPart:: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) per ottenere l'interfaccia **IDeviceTopology** per il dispositivo multiplexer di input.

Prima che l'utente possa registrare dal microfono nel diagramma precedente, l'applicazione client deve verificare che il multiplexer selezioni l'input del microfono. Nell'esempio di codice seguente viene illustrato come un client può attraversare il percorso dati dal microfono fino a quando non trova il multiplexer, che quindi programma per selezionare l'input del microfono:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



L'API DeviceTopology implementa un'interfaccia [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) per incapsulare un multiplexer, ad esempio quello nel diagramma precedente. Un'interfaccia [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) incapsula un Demultiplexer. Nell'esempio di codice precedente, il ciclo interno della funzione SelectCaptureDevice esegue una query su ogni unità secondaria che trova per individuare se la sottounità è un multiplexer. Se l'unità secondaria è un multiplexer, la funzione chiama il metodo [**IAudioInputSelector:: Seselection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) per selezionare l'input che si connette al flusso dal dispositivo dell'endpoint.

Nell'esempio di codice precedente, ogni iterazione del ciclo esterno attraversa una topologia del dispositivo. Quando si attraversano le topologie di dispositivo nel diagramma precedente, la prima iterazione attraversa il dispositivo multiplexer di input e la seconda iterazione attraversa il dispositivo di acquisizione Wave. La funzione verrà terminata quando raggiunge il connettore sul bordo destro del diagramma. La terminazione si verifica quando la funzione rileva un connettore con un \_ tipo di connessione io software. Questo tipo di connessione identifica il punto in cui il dispositivo adapter si connette al bus di sistema.

La chiamata al metodo [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) nell'esempio di codice precedente ottiene un valore di enumerazione **IPartType** che indica se la parte corrente è un connettore o una sottounità di elaborazione audio.

Il ciclo interno nell'esempio di codice precedente passa attraverso il collegamento da una parte alla successiva chiamando il metodo [**IPart:: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) . (Esiste anche un metodo [**IPart:: EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) per l'esecuzione di un'istruzione nella direzione opposta). Questo metodo recupera un oggetto [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) che contiene un elenco di tutte le parti in uscita. Tuttavia, qualsiasi parte che la funzione SelectCaptureDevice prevede di riscontrare in un dispositivo di acquisizione avrà sempre esattamente una parte in uscita. Quindi, la chiamata successiva a [**IPartsList:: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) richiede sempre la prima parte nell'elenco, il numero di parte 0, perché la funzione presuppone che questa sia l'unica parte nell'elenco.

Se la funzione SelectCaptureDevice rileva una topologia per la quale il presupposto non è valido, la funzione potrebbe non riuscire a configurare correttamente il dispositivo. Per evitare un errore di questo tipo, una versione più generica della funzione può eseguire le operazioni seguenti:

-   Chiamare il metodo [**IPartsList:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) per determinare il numero di parti in uscita.
-   Per ogni parte in uscita, chiamare **IPartsList:: GetPart** per iniziare a attraversare il percorso dati che conduce dalla parte.

Alcune parti, ma non necessariamente tutte, dispongono di controlli hardware associati che i client possono impostare o ottenere. Una particolare parte potrebbe avere zero, uno o più controlli hardware. Un controllo hardware è rappresentato dalla coppia di interfacce seguente:

-   Interfaccia di controllo generico, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), che dispone di metodi comuni a tutti i controlli hardware.
-   Interfaccia specifica della funzione (ad esempio, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) che espone i parametri di controllo per un particolare tipo di controllo hardware (ad esempio, un controllo del volume).

Per enumerare i controlli hardware per una parte, il client chiama prima il metodo [**IPart:: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) per determinare il numero di controlli hardware associati alla parte. Successivamente, il client effettua una serie di chiamate al metodo [**IPart:: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) per ottenere l'interfaccia **IControlInterface** per ogni controllo hardware. Infine, il client ottiene l'interfaccia specifica della funzione per ogni controllo hardware chiamando il metodo [**IControlInterface:: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) per ottenere l'ID di interfaccia. Il client chiama il metodo [**IPart:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) con questo ID per ottenere l'interfaccia specifica della funzione.

Una parte che è un connettore potrebbe supportare una delle seguenti interfacce di controllo specifiche della funzione:

-   [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

Una parte di un'unità secondaria potrebbe supportare una o più delle seguenti interfacce di controllo specifiche della funzione:

-   [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

Una parte supporta l'interfaccia **IDeviceSpecificProperty** solo se il controllo hardware sottostante ha un valore di controllo specifico del dispositivo e il controllo non può essere rappresentato in modo adeguato da nessun'altra interfaccia specifica della funzione nell'elenco precedente. In genere, una proprietà specifica del dispositivo è utile solo per un client in grado di dedurre il significato del valore della proprietà da informazioni quali il tipo di parte, il sottotipo della parte e il nome della parte. Il client può ottenere queste informazioni chiamando i metodi [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)e [**IPart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 

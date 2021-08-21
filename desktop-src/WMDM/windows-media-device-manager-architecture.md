---
title: Windows Architettura di Gestione dispositivi multimediali
description: Windows Architettura di Gestione dispositivi multimediali
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Gestione dispositivi multimediali, architettura
- Gestione dispositivi, architettura
- architettura per Windows Gestione dispositivi multimediali
- Windows Gestione dispositivi multimediali, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- Windows Gestione dispositivi multimediali, provider di servizi
- Gestione dispositivi, provider di servizi
- Windows Gestione dispositivi multimediali, plug-in
- Gestione dispositivi, plug-in
- applicazioni desktop, architettura Windows Gestione dispositivi multimediali
- provider di servizi, Windows'architettura di Gestione dispositivi multimediali
- plug-in, architettura Windows Gestione dispositivi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deadb7e5a85c4d7331a276a515add2ace30e566c2b683404b7b4466bf891dbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055604"
---
# <a name="windows-media-device-manager-architecture"></a>Windows Architettura di Gestione dispositivi multimediali

Windows Gestione dispositivi multimediali consente a un'applicazione o a un plug-in di comunicare con un dispositivo. Le applicazioni possono richiedere metadati del dispositivo, enumerare ed esplorare i dispositivi collegati e inviare o ricevere oggetti (cartelle, file, playlist e così via). Windows Gestione dispositivi multimediali fornisce una singola API all'applicazione chiamante, indipendentemente dal tipo di dispositivo chiamato (classe MTP o Mass Archiviazione, provider di servizi compilati sulla versione 10 o provider di servizi compilati in versioni precedenti di Windows Media Device Manager).

Windows Gestione dispositivi multimediali funge da punto di equilibrio tra i tre componenti principali del sistema: l'applicazione, che effettua richieste (per informazioni, per leggere o scrivere dati e così via); un provider di contenuti sicuro, ovvero un componente che gestisce la comunicazione con i file protetti da DRM; e un provider di servizi, che riceve le richieste dall'applicazione e comunica con il dispositivo per eseguire queste richieste. Sia l'applicazione che il provider di servizi si basano sull Windows SDK di Gestione dispositivi multimediali.

Il diagramma seguente illustra in che modo un'applicazione desktop comunica con un dispositivo Windows Gestione dispositivi multimediali 11.

![diagramma che mostra un'applicazione che comunica con quattro tipi diversi di dispositivi.](images/wmdm-device-communication.gif)

Il diagramma precedente mostra un'applicazione che comunica con quattro diversi tipi di dispositivi, ognuno con il proprio provider di servizi. Ogni provider di servizi è progettato per comunicare con un tipo specifico di dispositivo. Questo diagramma mostra i tre provider di servizi forniti da Microsoft (driver di classe generici per dispositivi di classe Mass Archiviazione, dispositivi RAPI e dispositivi MTP), nonché un provider di servizi personalizzato per un dispositivo proprietario creato da terze parti. Quando un dispositivo si connette, Windows Gestione dispositivi multimediali crea un'istanza del provider di servizi registrato per tale dispositivo. I provider di servizi ottengono le richieste dall'applicazione tramite Windows interfacce di Gestione dispositivi multimediali implementate, usano i driver appropriati per comunicare con il dispositivo e restituiscono risultati appropriati. La comunicazione tra il provider di servizi e il dispositivo non rientra nel dominio Windows Gestione dispositivi multimediali.

I provider di servizi sono invisibili all'applicazione. Un'applicazione visualizza solo un elenco di "dispositivi" perché Windows Gestione dispositivi multimediali espone un set standard di metodi e interfacce per tutti i dispositivi. Se un produttore crea un provider di servizi personalizzato, deve gestire tutti i metodi standard Windows Gestione dispositivi multimediali se le applicazioni devono essere in grado di usare il dispositivo.

Questo diagramma mostra anche un modulo SCP (Secure Content Provider). Questo modulo è responsabile della gestione del contenuto protetto da DRM (Digital Rights Management). Microsoft fornisce un modulo SCP in grado di gestire file WMA e WMV protetti da DRM. Se un'applicazione o un dispositivo intende gestire altri formati protetti, deve fornire il proprio modulo SCP. Né l'applicazione né il provider di servizi si occupa direttamente del provider di servizi.

Sia l'applicazione che il provider di servizi si basano su Windows Gestione dispositivi multimediali, che instrada le chiamate tra l'applicazione e il provider di servizi appropriato per un dispositivo; il provider di servizi è responsabile della comunicazione diretta con il dispositivo. Windows Gestione dispositivi multimediali esegue alcune azioni, ad esempio l'enumerazione dei dispositivi connessi, il routing delle chiamate e la gestione della verifica dei componenti. Tuttavia, la maggior parte delle operazioni viene eseguita dal provider di servizi, che riceve le richieste dall'applicazione e comunica con il dispositivo.

Un'applicazione compilata Windows Gestione dispositivi multimediali può comunicare con i dispositivi e i provider di servizi creati in versioni precedenti di Windows Media Device Manager; Tuttavia, questi dispositivi meno recenti verranno eseguiti tramite componenti della serie 9 (non visualizzati) e non supporteranno le funzionalità più recenti, in particolare la tecnologia di gestione dei diritti digitali più avanzata.

Architettura di un dispositivo

Il diagramma seguente mostra una gerarchia semplificata di dispositivi e risorse di archiviazione, come illustrato da un'applicazione che Windows Gestione dispositivi multimediali.

![diagramma che mostra le risorse di archiviazione in un dispositivo.](images/wmdm-basic-device-layout.gif)

Il diagramma precedente mostra una versione semplificata di un'unità flash connessa, come illustrato da un'Windows gestione dispositivi multimediali. L'unità flash ha attributi e proprietà, ad esempio un numero di serie e configurazioni di formato supportate. Un elemento figlio diretto del dispositivo flash è l'oggetto di archiviazione radice, che contiene una cartella, che a sua stessa contiene un'immagine e un brano.

Un'applicazione enumera l'elenco dei dispositivi collegati chiamando un metodo di enumerazione esposto [**dall'interfaccia IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) radice. I dispositivi sono rappresentati da [**un'interfaccia IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (o da un'interfaccia derivata). Questa interfaccia espone i metodi per recuperare il nome del dispositivo, le funzionalità di formato, il numero di serie e così via, nonché un metodo che enumera le risorse di *archiviazione* nel dispositivo. In Windows Gestione dispositivi multimediali, un archivio è qualsiasi tipo di oggetto nel dispositivo, indipendentemente dal fatto che si tratta di un BLOB di dati effettivo. Ad esempio: i file audio, i file di testo, le cartelle, le playlist archiviate come file e le playlist archiviate come metadati sono tutti considerati archivi, anche se le cartelle e gli elementi di metadati probabilmente non rappresentano un file fisico. Il tipo (o il formato) di una risorsa di archiviazione può essere recuperato chiamando [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (o [**GetMetadata,**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)richiedendo il formato dell'archiviazione).

Le risorse di archiviazione in un dispositivo vengono archiviate in modo gerarchico e tutti i dispositivi dispongono di un archivio radice. Ogni archiviazione può contenere zero o più oggetti figlio, enumerati chiamando il metodo [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) di tale archiviazione.

Si noti che a ogni archiviazione nel diagramma sono associati attributi e metadati (non vengono visualizzati tutti i valori). Gli attributi sono semplici informazioni booleane che spesso descrivono informazioni di gestione o navigazione (ad esempio "contiene cartelle" o "possono eliminare"), mentre i metadati possono essere valori stringa, numeri o informazioni complesse (ad esempio funzionalità di rendering). Gli attributi sono descritti da un set piuttosto limitato di flag definiti dall'SDK e recuperati chiamando [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2::GetAttributes2.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2) I valori dei metadati vengono recuperati con un nome univoco. L'SDK definisce una serie di valori di metadati che i dispositivi devono supportare, ma i dispositivi possono definire le proprie [costanti di metadati](metadata-constants.md). Tuttavia, se un dispositivo o un provider di servizi definisce una nuova costante di metadati, le applicazioni non saranno in grado di richiedere o impostare questo valore a meno che gli sviluppatori di applicazioni non siano a conoscenza di questa nuova costante. Un provider di servizi deve [**supportare IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) o versioni successive per supportare il recupero o l'impostazione dei metadati. Per altre informazioni, vedere [Recupero e impostazione di metadati e attributi.](getting-and-setting-metadata-and-attributes.md)

Provider di servizi

Il provider di servizi funge da intermediario tra l'applicazione e il dispositivo. Il provider di servizi è invisibile allo sviluppatore di applicazioni, quindi non è necessario che uno sviluppatore di applicazioni sappia nulla sullo sviluppo di un provider di servizi. Tuttavia, è il provider di servizi che esegue le operazioni di comunicazione con un dispositivo.

Un provider di servizi è una DLL COM compilata Windows Gestione dispositivi multimediali che riceve le richieste da un'applicazione e comunica con il dispositivo per eseguirle. La comunicazione con l'applicazione desktop viene mediata Windows Gestione dispositivi multimediali; la comunicazione con il dispositivo è sotto il controllo del provider di servizi.

Un provider di servizi riceve richieste dall'applicazione per enumerare il contenuto del dispositivo, richieste di funzionalità del dispositivo, richieste di lettura o scrittura dei dati e così via. Deve conoscere la progettazione di un dispositivo abbastanza da poter inviare comandi nel formato e nel protocollo corretto. Dovrebbe anche essere in grado di nascondere i requisiti specifici del dispositivo, ad esempio un'estensione di file necessaria per le playlist, in modo che le applicazioni non debbano conoscere questi requisiti per poter usare il dispositivo.

Microsoft offre diversi provider di servizi per i tipi di dispositivi standard, tra cui dispositivi MTP generici, dispositivi di Archiviazione di massa e dispositivi RAPI. L'unico motivo per cui un progettista di dispositivi deve creare un provider di servizi personalizzato è se un dispositivo presenta requisiti di archiviazione dati specifici o insoliti che i provider di servizi standard non gestiscono, ad esempio se i file devono essere archiviati in posizioni specifiche e il sistema operativo del dispositivo non gestisce automaticamente questa operazione.

Quando un dispositivo è connesso al computer, il sistema operativo crea un'istanza del provider di servizi appropriato per ogni applicazione Windows Gestione dispositivi multimediali. Se viene avviata Windows'applicazione Gestione dispositivi multimediali, verrà caricata una seconda istanza del provider di servizi. Tuttavia, ogni provider di servizi può gestire più dispositivi. come illustrato nel diagramma seguente.

![diagramma che mostra due dispositivi mtp che comunicano con due applicazioni.](images/wmdm-sp-to-device.gif)

Il diagramma precedente mostra due diverse applicazioni che comunicano con due dispositivi MTP. I dispositivi usano la stessa classe del provider di servizi, ma ogni applicazione ha una propria istanza dello stesso provider di servizi. Ogni istanza del provider di servizi comunica con i dispositivi. Le diverse istanze del provider di servizi non sono a conoscenza l'una dell'altra.

Molti metodi dell'applicazione hanno un metodo del provider di servizi denominato in modo corrispondente. Quando l'applicazione chiama un metodo, Windows Gestione dispositivi multimediali instrada la chiamata al metodo corrispondente nel provider di servizi (anche se potrebbe eseguire prima alcune azioni interne aggiuntive). Ad esempio, quando l'applicazione chiama [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty), Windows Gestione dispositivi multimediali instrada questa chiamata all'implementazione del provider di servizi [**di IMDSPDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty). La maggior parte delle interfacce dell'applicazione inizia con IWMDM e l'interfaccia del provider di servizi corrispondente inizia con IMDSP. È previsto che il provider di servizi gestirà questa chiamata al metodo e restituirà un risultato appropriato.

Un'applicazione non esplora o comunica mai direttamente con un dispositivo (a meno che non chiami [**IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) o [**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)); l'applicazione comunica con il provider di servizi, che deve rappresentare un dispositivo nel modo più logico e semplice possibile. Quando l'applicazione richiede informazioni sul dispositivo o enumera gli oggetti nel dispositivo, il provider di servizi esegue una query sul dispositivo in modo appropriato e acquisisce e restituisce le informazioni appropriate. Può esporre l'organizzazione di file nel dispositivo in modo diverso da come viene fisicamente archiviato nel dispositivo, se appropriato. Tuttavia, espone il dispositivo, deve essere in modo coerente e logico, per consentire all'applicazione di trovare le informazioni necessarie e gestire i comandi inviati. Un buon provider di servizi nasconde le particolarità specifiche del dispositivo, ad esempio se il dispositivo archivia fisicamente una playlist come file con un'estensione di file personalizzata, il provider di servizi deve aggiungere automaticamente tale estensione quando l'applicazione crea una playlist nel dispositivo; non deve aspettarsi che l'applicazione sappia l'estensione appropriata durante la creazione di un oggetto playlist.

I provider di servizi vengono eseguiti all'interno del processo dell'applicazione chiamante. L'unica eccezione è il provider di servizi MTP, che viene eseguito nel proprio processo. Per questo motivo, esiste un rischio che un provider di servizi bloccato causerà il blocco dell'applicazione chiamante. Pertanto, i provider di servizi devono essere progettati per essere affidabili e impedire il blocco e le applicazioni devono essere progettate per evitare che si blocchino se una particolare chiamata al metodo non viene restituita rapidamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività iniziali**](getting-started.md)
</dt> </dl>

 

 





---
title: Architettura di Windows Media Gestione dispositivi
description: Architettura di Windows Media Gestione dispositivi
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Media Gestione dispositivi, architettura
- Gestione dispositivi, architettura
- architettura per Windows Media Gestione dispositivi
- Windows Media Gestione dispositivi, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- Windows Media Gestione dispositivi, provider di servizi
- Gestione dispositivi, provider di servizi
- Windows Media Gestione dispositivi, plug-in
- Gestione dispositivi, plug-in
- applicazioni desktop, architettura Windows Media Gestione dispositivi
- provider di servizi, architettura di Windows Media Gestione dispositivi
- plug-in, architettura di Windows Media Gestione dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fda87e4ed4bce2c82bbb9c0863c119851965940
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221159"
---
# <a name="windows-media-device-manager-architecture"></a>Architettura di Windows Media Gestione dispositivi

Windows Media Gestione dispositivi consente a un'applicazione o a un plug-in di comunicare con un dispositivo. Le applicazioni possono richiedere i metadati del dispositivo, enumerare ed esplorare i dispositivi collegati e inviare o ricevere oggetti (cartelle, file, playlist e così via). Windows Media Gestione dispositivi fornisce un'unica API all'applicazione chiamante, indipendentemente dal tipo di dispositivo chiamato (MTP o classe di archiviazione di massa, provider di servizi basati sulla versione 10 o provider di servizi basati su versioni precedenti di Windows Media Gestione dispositivi).

Windows Media Gestione dispositivi funge da intermediario per i tre componenti principali del sistema: l'applicazione, che effettua richieste (per informazioni, leggere o scrivere dati e così via); un provider di contenuti protetto, ovvero un componente che gestisce la comunicazione con file protetti da DRM; e un provider di servizi, che riceve le richieste dall'applicazione e comunica con il dispositivo per eseguire queste richieste. Sia l'applicazione che il provider di servizi sono basati su Windows Media Gestione dispositivi SDK.

Il diagramma seguente illustra il modo in cui un'applicazione desktop comunica con un dispositivo usando Windows Media Gestione dispositivi 11.

![diagramma che mostra un'applicazione che comunica con quattro tipi diversi di dispositivi.](images/wmdm-device-communication.gif)

Il diagramma precedente mostra un'applicazione che comunica con quattro tipi diversi di dispositivi, ognuno con il proprio provider di servizi. Ogni provider di servizi è progettato per comunicare con un tipo specifico di dispositivo; Questo diagramma illustra i tre provider di servizi forniti da Microsoft (driver di classe generici per i dispositivi di classe di archiviazione di massa, i dispositivi RAPI e i dispositivi MTP), nonché un provider di servizi personalizzato per un dispositivo proprietario creato da terze parti. Quando un dispositivo si connette, Windows Media Gestione dispositivi crea un'istanza del provider di servizi registrato per tale dispositivo. I provider di servizi ottengono richieste dall'applicazione tramite Windows Media Gestione dispositivi interfacce implementate, usano i driver appropriati per comunicare con il dispositivo e restituiscono risultati appropriati. La comunicazione tra il provider di servizi e il dispositivo esula dal dominio di Windows Media Gestione dispositivi.

I provider di servizi sono invisibili all'applicazione; in un'applicazione viene visualizzato solo un elenco di "dispositivi" poiché Windows Media Gestione dispositivi espone un set standard di metodi e interfacce per tutti i dispositivi. Se un produttore crea un provider di servizi personalizzato, deve gestire tutti i metodi Windows Media Gestione dispositivi standard se le applicazioni devono essere in grado di usare il dispositivo.

Questo diagramma mostra anche un modulo SCP (Secure Content Provider). Questo modulo è responsabile della gestione dei contenuti protetti Digital Rights Management (DRM). Microsoft fornisce un modulo SCP in grado di gestire file WMA e WMV protetti da DRM. Se un'applicazione o un dispositivo intende gestire altri formati protetti, deve fornire il proprio modulo SCP. Né l'applicazione né il provider di servizi si occupano direttamente dell'SCP.

Sia l'applicazione che il provider di servizi sono basati su Windows Media Gestione dispositivi, che instrada le chiamate tra l'applicazione e il provider di servizi appropriato per un dispositivo; il provider di servizi è responsabile della comunicazione diretta con il dispositivo. Windows Media Gestione dispositivi esegue alcune azioni, ad esempio l'enumerazione dei dispositivi connessi, le chiamate di routing e la gestione della verifica dei componenti. Tuttavia, la maggior parte del lavoro viene eseguita dal provider di servizi, che riceve le richieste dall'applicazione e comunica con il dispositivo.

Un'applicazione basata su Windows Media Gestione dispositivi può comunicare con i dispositivi e i provider di servizi compilati in versioni precedenti di Windows Media Gestione dispositivi; Tuttavia, questi dispositivi meno recenti verranno eseguiti con i componenti della serie 9 (non mostrati) e non supporteranno le funzionalità più recenti, in particolare la tecnologia Digital Rights Management più avanzata.

Architettura di un dispositivo

Il diagramma seguente mostra una gerarchia semplificata dei dispositivi e delle archiviazioni come visto da un'applicazione che usa Windows Media Gestione dispositivi.

![diagramma che mostra le archiviazioni in un dispositivo.](images/wmdm-basic-device-layout.gif)

Il diagramma precedente mostra una versione semplificata di un'unità flash connessa, come visto da un'applicazione Windows Media Gestione dispositivi. L'unità flash contiene attributi e proprietà, ad esempio un numero di serie e configurazioni di formato supportate. Un figlio immediato del dispositivo flash è l'oggetto di archiviazione radice, che contiene una cartella, che a sua volta contiene un'immagine e un brano.

Un'applicazione enumera l'elenco di dispositivi collegati chiamando un metodo di enumerazione esposto dall'interfaccia [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) radice. I dispositivi sono rappresentati da un'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (o derivata). Questa interfaccia espone i metodi per recuperare il nome del dispositivo, le funzionalità di formattazione, il numero di serie e così via, nonché un metodo che enumera le *archiviazioni* sul dispositivo. In Windows Media Gestione dispositivi, una risorsa di archiviazione è qualsiasi tipo di oggetto nel dispositivo, indipendentemente dal fatto che si tratti di un BLOB di dati effettivo. Ad esempio, i file audio, i file di testo, le cartelle, le playlist archiviate come file e le playlist archiviate come metadati sono tutti considerati archiviazione, anche se le cartelle e gli elementi di metadati probabilmente non rappresentano un file fisico. Il tipo o il formato di un'archiviazione può essere recuperato chiamando [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (o [**GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata), richiedendo il formato di archiviazione).

Le archiviazioni in un dispositivo vengono archiviate in modo gerarchico e tutti i dispositivi hanno un archivio radice. Ogni archiviazione può ospitare zero o più oggetti figlio, enumerati chiamando il metodo [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) dell'archiviazione.

Si noti che a ogni archiviazione nel diagramma sono associati attributi e metadati (non tutti i valori vengono visualizzati). Gli attributi sono semplici informazioni booleane che spesso descrivono le informazioni di gestione o di spostamento (ad esempio "has Folders&quot; o &quot;can delete"), mentre i metadati possono essere valori stringa, numeri o informazioni complesse, ad esempio le funzionalità di rendering. Gli attributi vengono descritti da un set di flag piuttosto limitati definito dall'SDK e recuperati chiamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). I valori dei metadati vengono recuperati con un nome univoco. l'SDK definisce un numero di valori di metadati che i dispositivi devono supportare, ma i dispositivi possono definire le proprie [costanti di metadati](metadata-constants.md). Tuttavia, se un dispositivo o un provider di servizi definisce una nuova costante di metadati, le applicazioni non saranno in grado di richiedere o impostare questo valore a meno che gli sviluppatori di applicazioni non siano a conoscenza di questa nuova costante. Per supportare il recupero o l'impostazione dei metadati, un provider di servizi deve supportare [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) o versioni successive. Per altre informazioni, vedere [Getting and setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).

Provider di servizi

Il provider di servizi funge da intermediario tra l'applicazione e il dispositivo. Il provider di servizi è invisibile allo sviluppatore di applicazioni, quindi uno sviluppatore di applicazioni non deve sapere nulla sullo sviluppo di un provider di servizi. Tuttavia, si tratta del provider di servizi che esegue le comunicazioni con un dispositivo.

Un provider di servizi è una DLL COM basata su Windows Media Gestione dispositivi che riceve le richieste da un'applicazione e comunica con il dispositivo per eseguirle. La comunicazione con l'applicazione desktop è mediata da Windows Media Gestione dispositivi; la comunicazione con il dispositivo è sotto il controllo del provider di servizi.

Un provider di servizi riceve le richieste dall'applicazione per enumerare il contenuto del dispositivo, le richieste per le funzionalità del dispositivo, le richieste di lettura o scrittura dei dati e così via. Deve essere a conoscenza della progettazione di un dispositivo in grado di inviare comandi nel formato e nel protocollo appropriati. Deve anche essere in grado di nascondere i requisiti specifici del dispositivo, ad esempio un'estensione di file necessaria per le playlist, in modo che le applicazioni non debbano essere a conoscenza di questi requisiti per poter usare il dispositivo.

Microsoft fornisce diversi provider di servizi per i tipi di dispositivi standard, inclusi i dispositivi MTP generici, i dispositivi di classe di archiviazione di massa e i dispositivi RAPI. Il solo motivo per cui un progettista di dispositivi deve creare un provider di servizi personalizzato è se un dispositivo presenta requisiti di archiviazione dati specifici o insoliti che non vengono gestiti dai provider di servizi standard, ad esempio se i file devono essere archiviati in percorsi specifici e il sistema operativo del dispositivo non la gestisce automaticamente.

Quando un dispositivo è connesso al computer, il sistema operativo crea un'istanza del provider di servizi appropriato per ogni applicazione Windows Media Gestione dispositivi. Se viene avviata una seconda applicazione Windows Media Gestione dispositivi, viene caricata una seconda istanza del provider di servizi. Tuttavia, ogni provider di servizi è in grado di gestire più dispositivi. come illustrato nel diagramma seguente.

![diagramma che mostra due dispositivi MTP che comunicano con due applicazioni.](images/wmdm-sp-to-device.gif)

Il diagramma precedente mostra due applicazioni diverse che comunicano con due dispositivi MTP. I dispositivi usano la stessa classe del provider di servizi, ma ogni applicazione dispone di una propria istanza dello stesso provider di servizi. Ogni istanza del provider di servizi sta comunicando con i dispositivi. Le diverse istanze del provider di servizi non sono consapevoli l'una dall'altra.

Molti metodi dell'applicazione hanno un metodo del provider di servizi denominato corrispondente. Quando l'applicazione chiama un metodo, Windows Media Gestione dispositivi instrada la chiamata al metodo corrispondente sul provider di servizi (anche se potrebbe eseguire prima alcune azioni interne aggiuntive). Ad esempio, quando l'applicazione chiama [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty), Windows Media Gestione dispositivi instrada questa chiamata all'implementazione del provider di servizi di [**IMDSPDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty). La maggior parte delle interfacce dell'applicazione inizia con IWMDM e l'interfaccia del provider di servizi corrispondente inizia con IMDSP). È previsto che il provider di servizi gestisca la chiamata al metodo e restituisca un risultato appropriato.

Un'applicazione non Esplora né comunica direttamente con un dispositivo (a meno che non chiami [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) o [**IWMDMStorage:: SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)); l'applicazione comunica con il provider di servizi, che deve rappresentare un dispositivo nel modo più logico e semplice possibile. Quando l'applicazione richiede informazioni sul dispositivo o enumera gli oggetti nel dispositivo, il provider di servizi esegue una query sul dispositivo in modo appropriato e acquisisce e restituisce le informazioni appropriate. È possibile che l'organizzazione di file nel dispositivo venga esposta in modo diverso rispetto alla modalità di archiviazione fisica del dispositivo, se appropriato. Tuttavia, il dispositivo viene esposto in modo coerente e logico, per consentire all'applicazione di trovare le informazioni necessarie e gestire i comandi inviati. Un provider di servizi valido nasconde le peculiarità specifiche del dispositivo, ad esempio se il dispositivo archivia fisicamente una playlist come file con un'estensione di file personalizzata, il provider di servizi deve aggiungere automaticamente tale estensione quando l'applicazione crea una playlist nel dispositivo. Quando si crea un oggetto playlist, l'applicazione non deve essere in grado di conoscerne l'estensione corretta.

I provider di servizi vengono eseguiti nel processo dell'applicazione chiamante. L'unica eccezione è rappresentata dal provider di servizi MTP, che viene eseguito nel proprio processo. Per questo motivo, esiste il rischio che un provider di servizi bloccati provochi il blocco dell'applicazione chiamante. Pertanto, i provider di servizi devono essere progettati in modo da essere affidabili e impedire il blocco e le applicazioni devono essere progettate in modo da evitare il blocco se una particolare chiamata al metodo non restituisce rapidamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Introduzione**](getting-started.md)
</dt> </dl>

 

 





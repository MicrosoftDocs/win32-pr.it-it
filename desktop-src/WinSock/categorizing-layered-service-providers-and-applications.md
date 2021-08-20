---
title: Categorizzazione di app e provider di servizi a più livelli
description: Winsock 2 supporta protocolli a più livelli.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993b7a4003b87cf902b9daccbea4742a0bcd0760642429db79b1f1bb0a22600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322392"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Categorizzazione di app e provider di servizi a più livelli

> [!Note]  
> I provider di servizi su più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform.](../fwp/windows-filtering-platform-start-page.md)

 

Winsock 2 supporta protocolli a più livelli. Un protocollo a più livelli implementa solo funzioni di comunicazione di livello superiore, basandosi allo stesso tempo su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto. Un esempio di protocollo a più livelli o provider di servizi a più livelli è un livello di sicurezza che aggiunge il protocollo al processo di definizione della connessione per eseguire l'autenticazione e stabilire uno schema di crittografia concordato a livello reciproco. Un protocollo di sicurezza di questo tipo richiede in genere i servizi di un protocollo di trasporto affidabile sottostante, ad esempio TCP o SPX. Il termine protocollo di base implementato dal provider di base si riferisce a un provider Winsock che implementa un protocollo come TCP o SPX in grado di eseguire comunicazioni dati con un endpoint remoto. Il termine protocollo a più livelli viene usato per descrivere un protocollo che non può essere autonomo. Questi protocolli su più livelli vengono installati come provider di servizi a più livelli (LSP) Winsock.

Un esempio di LSP è Client Microsoft Firewall Service Provider installato come parte del server di autenticazione (ISA) Internet nei client. Il Client Microsoft Firewall service provider viene installato sui provider di base Winsock per TCP e UDP. Una libreria a collegamento dinamico (DLL) nel software client firewall ISA diventa un provider di servizi a più livelli Winsock che tutte le applicazioni Winsock usano in modo trasparente. In questo modo, l'LSP del client firewall ISA può intercettare le chiamate di funzione Winsock dalle applicazioni client e quindi instradare una richiesta al provider di servizi di base originale se la destinazione è locale o al servizio Firewall in un computer ISA Server se la destinazione è remota. Un provider di servizi di configurazione simile viene installato come parte del servizio Microsoft Forefront Firewall e del client Threat Management Gateway (TMG) nei client.

Durante l'inizializzazione dell'LSP, l'LSP deve fornire puntatori a una serie di funzioni SPI (Service Provider Interface) Winsock. Queste funzioni verranno chiamate durante la normale elaborazione dal livello direttamente sopra l'LSP (un altro LSP o Ws2 \_32.DLL).

È possibile definire categorie LSP in base al subset di funzioni SPI implementate da un LSP e alla natura dell'elaborazione aggiuntiva eseguita per ognuna di queste funzioni. Classificando i provider di servizi di configurazione e classificando le applicazioni che usano socket Winsock, diventa possibile determinare in modo selettivo se un LSP deve essere coinvolto in un determinato processo in fase di esecuzione.

In Windows Vista e versioni successive viene fornito un nuovo metodo per classificare sia i provider di servizi a livelli Winsock che le applicazioni in modo che verranno caricati solo determinati LSP. Esistono diversi motivi per aggiungere queste funzionalità.

Uno dei motivi principali è che alcuni processi critici del sistema, ad esempio winlogon e lsass, creano socket, ma questi processi non usano questi socket per inviare traffico in rete. La maggior parte dei file LSP non deve quindi essere caricata in questi processi. Sono stati documentati anche alcuni casi in cui i LSP con problemi possono causarelsass.exe *arresto* anomalo. Se lsass si arresta in modo anomalo, il sistema forza un arresto. Un effetto collaterale di questi processi di sistema che caricano LSP è che questi processi non vengono mai terminati, quindi quando un LSP viene installato o rimosso, è necessario un riavvio.

Un motivo secondario è che in alcuni casi le applicazioni potrebbero non voler caricare determinati LSP. Ad esempio, alcune applicazioni potrebbero non voler caricare gli LSP crittografici che potrebbero impedire all'applicazione di comunicare con altri sistemi in cui non è installato l'LSP ciptografico.

Infine, le categorie LSP possono essere usate da altri provider di servizi di sicurezza per determinare dove installare se stessi nella catena di protocolli Winsock. Per anni, diversi sviluppatori LSP hanno desiderato un modo per sapere come si comporterà un LSP. Ad esempio, un provider di servizi di configurazione che controlla il flusso di dati deve essere superiore a un LSP che crittografa i dati. Naturalmente, questo metodo di categorizzazione LSP non è una prova insoddibile perché si basa su LSP di terze parti per classificarsi in modo appropriato.

La categorizzazione LSP e altri miglioramenti della sicurezza in Windows Vista e versioni successive sono progettati per impedire agli utenti di installare involontariamente LSP dannosi.

## <a name="lsp-categories"></a>Categorie LSP

In Windows Vista e versioni successive, un LSP può essere classificato in base al modo in cui interagisce con le chiamate e i dati Windows Sockets. Una categoria LSP è un gruppo identificabile di comportamenti in un subset di funzioni SPI winsock. Ad esempio, un filtro contenuto HTTP viene categorizzato come controllo dati (categoria LSP \_ INSPECTOR). La categoria LSP \_ INSPECTOR ispeziona (ma non modifica) i parametri nelle funzioni SPI di trasferimento dei dati. Un'applicazione può eseguire una query per la categoria di un LSP e scegliere di non caricare l'LSP in base alla categoria LSP e al set di categorie LSP consentite dell'applicazione.

Nella tabella seguente sono elencate le categorie in cui è possibile classificare un provider di servizi di distribuzione.

| Categoria LSP              | Descrizione                                                     |
|---------------------------|-----------------------------------------------------------------|
| **LSP \_ CRYPTO \_ COMPRESS** | LSP è un provider di crittografia o di compressione dei dati.         |
| **LSP \_ FIREWALL**         | LSP è un provider di firewall.                                 |
| **LSP \_ LOCAL \_ CACHE**     | LSP è un provider di cache locale.                              |
| **LSP \_ INBOUND \_ MODIFY**  | LSP modifica i dati in ingresso.                                  |
| **LSP \_ INSPECTOR**        | Il provider di servizi di configurazione (LSP) esamina o filtra i dati.                               |
| **LSP \_ OUTBOUND \_ MODIFY** | L'LSP modifica i dati in uscita.                                 |
| **LSP \_ PROXY**            | LSP funge da proxy e reindirizza i pacchetti.                  |
| **LSP \_ REDIRECTOR**       | LSP è un redirector di rete.                                |
| **LSP \_ SYSTEM**           | L'LSP è accettabile per l'uso nei servizi e nei processi di sistema. |



 

Un LSP può appartenere a più di una categoria. Ad esempio, un provider di servizi di configurazione firewall/sicurezza può appartenere sia alle categorie di controllo (**LSP \_ INSPECTOR**) che al firewall (**LSP \_ FIREWALL**).

Se per un provider di servizi di configurazione non è impostata una categoria, viene considerato nella categoria Tutti gli altri. Questa categoria LSP non verrà caricata nei servizi o nei processi di sistema(ad esempio, lsass, winlogon e molti processi svchost).

## <a name="categorizing-lsps"></a>Categorizzazione di LSP

In Vista e versioni successive sono Windows disponibili diverse nuove funzioni per la categorizzazione di un LSP:

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Per classificare un LSP, la funzione [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) o [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) viene chiamata con un GUID per identificare la voce nascosta LSP, la classe di informazioni da impostare per questa voce del protocollo LSP e un set di flag usati per modificare il comportamento della funzione.

La [**funzione WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) o [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) viene usata in modo analogo per recuperare i dati associati a una classe di informazioni per un LSP.

## <a name="categorizing-applications"></a>Categorizzazione delle applicazioni

Sono disponibili diverse nuove funzioni in Windows Vista e versioni successive per la categorizzazione di un'applicazione:

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Per classificare un'applicazione, la funzione [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) viene chiamata con il percorso di caricamento dell'immagine eseguibile per identificare l'applicazione, gli argomenti della riga di comando usati all'avvio dell'applicazione e le categorie LSP consentite per tutte le istanze di questa applicazione.

La [**funzione WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) viene usata in modo analogo per recuperare le categorie del provider di servizi a più livelli (LSP) associate a un'applicazione.

## <a name="determining-which-lsps-get-loaded"></a>Determinazione dei file LSP caricati

L'ultima parte della categorizzazione LSP è determinare quali LSP verranno caricati in quali processi. Quando un processo carica Winsock, vengono effettuati i confronti seguenti tra la categoria dell'applicazione e le categorie LSP per tutti i provider di servizi di configurazione installati:

-   Se l'applicazione non è categorizzata, consentire il caricamento di tutti i file LSP nel processo.
-   Se all'applicazione e all'LSP sono assegnate categorie, è necessario che siano vere tutte le condizioni seguenti: <dl> Almeno una delle categorie LSP è presente nelle categorie specificate dell'applicazione.  
    Solo le categorie specificate nelle categorie specificate dell'applicazione vengono specificate nelle categorie LSP. Ad esempio, se l'applicazione specifica una categoria, deve essere nella categoria dell'LSP.  
    Se la categoria LSP SYSTEM è presente nella categoria dell'applicazione, deve essere \_ presente nelle categorie dell'LSP.  
    </dl>

> [!Note]  
> Se un LSP non è categorizzato, la relativa categoria è effettivamente zero. Perché si verifichi una corrispondenza, tutte le categorie specificate del provider di servizi di configurazione locale devono essere presenti nelle categorie dell'applicazione (le categorie dell'applicazione devono essere un superset delle categorie del provider di servizi di configurazione locale) con l'avvertenza che se LSP SYSTEM è presente nella categoria dell'applicazione deve essere presente anche nella categoria \_ dell'LSP.

 

Si consideri l'esempio seguente:

LFoo.exeappalto è classificata come LSP SYSTEM +  \_ LSP FIREWALL + \_ LSP CRYPTO \_ \_ COMPRESS. *L'applicazioneBar.exe* è classificata come LSP \_ FIREWALL + LSP CRYPTO \_ \_ COMPRESS. Nel sistema sono installati quattro LSP:

-   LSP1 ha impostato una categoria di LSP \_ SYSTEM.
-   LSP2 non è impostato su categorie, quindi la categoria è zero.
-   LSP3 ha impostato una categoria di FIREWALL \_ LSP.
-   LSP4 ha impostato categorie di LSP \_ SYSTEM + LSP \_ FIREWALL + LSP CRYPTO COMPRESS \_ + \_ \_ LSP INSPECTOR

In questo esempio *l'applicazioneFoo.exe* carica solo LSP1, mentre l'applicazione *Bar.exe* carica LSP3.

## <a name="determining-winsock-providers-installed"></a>Determinazione dei provider Winsock installati

Microsoft Windows Software Development Kit (SDK) include un programma Winsock di esempio che può essere usato per determinare i provider di trasporto Winsock installati in un computer locale. Per impostazione predefinita, il codice sorgente per questo esempio Winsock viene installato nella directory seguente di Windows SDK per Windows 7:

*C: \\ Programmi \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ NetDs \\ winsock \\ LSP*

Questo esempio è un'utilità per l'installazione e il test di provider di servizi a più livelli. Ma può anche essere usato per raccogliere informazioni dettagliate a livello di codice dal catalogo Winsock in un computer locale. Per elencare tutti i provider Winsock correnti, inclusi i provider di base e i provider di servizi di livello, compilare questo esempio winsock ed eseguire il comando della console seguente:

**instlsp -p**

L'output sarà un elenco di provider Winsock installati nel computer locale, inclusi i provider di servizi a più livelli. L'output elenca l'ID catalogo e il nome della stringa per il provider Winsock

Per raccogliere informazioni più dettagliate su tutti i provider Winsock, eseguire il comando della console seguente:

**instlsp -p -v**

L'output sarà un elenco [**di strutture WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) supportate nel computer locale.

Per un elenco dei soli provider di servizi su più livelli installati nel computer locale, eseguire il comando della console seguente:

**instlsp -l**

Per eseguire il mapping della struttura LSP, eseguire il comando della console seguente:

**instlsp -m**

> [!Note]  
> La funzionalità TDI è deprecata e verrà rimossa nelle versioni future di Microsoft Windows. A seconda di come si usa TDI, usare il kernel Winsock (WSK) o Windows Filtering Platform (WFP). Per altre informazioni su WFP e WSK, [vedere Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md) e [Winsock Kernel.](/windows-hardware/drivers/ddi/_netvista/) Per un Windows core networking su WSK e TDI, vedere [Introduction to Winsock Kernel (WSK) (Introduzione al kernel Winsock - WSK).](/archive/blogs/wndp/)

 

 

 

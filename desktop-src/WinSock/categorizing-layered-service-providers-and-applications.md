---
title: Categorizzazione di app e provider di servizi a più livelli
description: Winsock 2 supporta i protocolli a livelli.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a966d54da0be26f75a074de18abe1b9e080c0c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307023"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Categorizzazione di app e provider di servizi a più livelli

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

Winsock 2 supporta i protocolli a livelli. Un protocollo a più livelli è uno che implementa solo funzioni di comunicazione di livello superiore, mentre si basa su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto. Un esempio di protocollo a più livelli o di un provider di servizi su più livelli è un livello di sicurezza che aggiunge il protocollo al processo di creazione della connessione per poter eseguire l'autenticazione e stabilire uno schema di crittografia concordato a vicenda. Un protocollo di sicurezza di questo tipo richiede in genere i servizi di un protocollo di trasporto affidabile sottostante, ad esempio TCP o SPX. Il termine protocollo di base implementato dal provider di base fa riferimento a un provider Winsock che implementa un protocollo, ad esempio TCP o SPX, che è in grado di eseguire le comunicazioni dati con un endpoint remoto. Il termine protocollo a più livelli viene usato per descrivere un protocollo che non può essere autonomo. Questi protocolli a più livelli vengono installati come provider di servizi a più livelli Winsock (LSP).

Un esempio di LSP è il provider di servizi client di Microsoft Firewall installato come parte di Internet secutity e Authentication Server (ISA) sui client. Il provider di servizi client di Microsoft Firewall viene installato sui provider di base Winsock per TCP e UDP. Una libreria di collegamento dinamico (DLL) nel software client ISA Firewall diventa un provider di servizi a più livelli Winsock che tutte le applicazioni Winsock utilizzano in modo trasparente. In questo modo, il client ISA Firewall LSP può intercettare le chiamate di funzione Winsock dalle applicazioni client e quindi indirizzare una richiesta al provider del servizio di base sottostante originale se la destinazione è locale o al servizio firewall in un computer ISA Server se la destinazione è remota. Un LSP simile viene installato come parte del servizio Microsoft Forefront firewall e del client di Threat Management Gateway (TMG) sui client.

Durante l'inizializzazione di LSP, lo LSP deve fornire puntatori a una serie di funzioni di interfaccia del provider di servizi (SPI) Winsock. Queste funzioni verranno chiamate durante la normale elaborazione da parte del livello immediatamente superiore a LSP (un altro LSP o WS2 \_32.DLL).

È possibile definire le categorie LSP basate sul subset di funzioni SPI implementate da LSP e sulla natura dell'elaborazione aggiuntiva eseguita per ognuna di queste funzioni. Classificando LSP, oltre a classificare le applicazioni che usano i socket Winsock, è possibile determinare in modo selettivo se uno LSP deve essere associato a un determinato processo in fase di esecuzione.

In Windows Vista e versioni successive viene fornito un nuovo metodo per la categorizzazione di applicazioni e provider di servizi a più livelli Winsock, in modo che vengano caricati solo determinati LSP. Esistono diversi motivi per aggiungere queste funzionalità.

Uno dei motivi principali è che alcuni processi critici del sistema, ad esempio Winlogon e LSASS creano socket, ma questi processi non utilizzano questi socket per inviare traffico sulla rete. Quindi, la maggior parte dei LSP non deve essere caricata in questi processi. È stato inoltre documentato un numero di casi in cui la LSP di bug può causare l'arresto anomalo *lsass.exe* . Se LSASS si arresta in modo anomalo, il sistema impone un arresto. Un effetto collaterale di questi processi di sistema durante il caricamento di LSP è che questi processi non vengono mai chiusi, quindi è necessario riavviare il computer quando viene installato o rimosso uno LSP.

Un motivo secondario è che in alcuni casi è possibile che le applicazioni non desiderino caricare determinati LSP. Ad esempio, alcune applicazioni potrebbero non voler caricare lsp crittografici, che potrebbero impedire la comunicazione dell'applicazione con altri sistemi in cui non è installato il cyptographic LSP.

Infine, le categorie LSP possono essere utilizzate da altri LSP per determinare la posizione della catena di protocollo Winsock da installare. Per anni, diversi sviluppatori di LSP hanno voluto conoscere il comportamento di uno LSP. Ad esempio, un LSP che controlla il flusso di dati deve essere superiore a uno LSP che crittografa i dati. Naturalmente, questo metodo per la categorizzazione di LSP non è una prova, perché si basa su LSP di terze parti per categorizzare se stesso in modo appropriato.

La categorizzazione di LSP e altri miglioramenti della sicurezza in Windows Vista e versioni successive sono progettati per impedire agli utenti di installare involontariamente LSP dannosi.

## <a name="lsp-categories"></a>Categorie LSP

In Windows Vista e versioni successive, un LSP può essere classificato in base al modo in cui interagisce con le chiamate e i dati di Windows Sockets. Una categoria LSP è un gruppo di comportamenti identificabili in un subset di funzioni Winsock SPI. Un filtro di contenuto HTTP, ad esempio, verrebbe categorizzato come controllo dati (categoria di \_ controllo LSP). La \_ categoria di controllo LSP controlla (ma non modifica) i parametri per le funzioni SPI per il trasferimento dei dati. Un'applicazione può eseguire una query per la categoria di un LSP e scegliere di non caricare il LSP in base alla categoria LSP e al set di categorie di LSP consentite dell'applicazione.

Nella tabella seguente sono elencate le categorie in cui è possibile classificare LSP.

| Categoria LSP              | Descrizione                                                     |
|---------------------------|-----------------------------------------------------------------|
| **\_compressione crittografica LSP \_** | LSP è un provider di crittografia o di compressione dei dati.         |
| **\_Firewall LSP**         | LSP è un provider del firewall.                                 |
| **\_cache locale \_ LSP**     | LSP è un provider di cache locale.                              |
| **\_modifica in ingresso \_ LSP**  | Il LSP modifica i dati in ingresso.                                  |
| **\_controllo LSP**        | Il LSP controlla o filtra i dati.                               |
| **\_modifica in uscita \_ LSP** | Il LSP modifica i dati in uscita.                                 |
| **\_proxy LSP**            | Il LSP funge da proxy e reindirizza i pacchetti.                  |
| **redirector LSP \_**       | LSP è un redirector di rete.                                |
| **\_sistema LSP**           | Il LSP è accettabile per l'uso nei servizi e nei processi di sistema. |



 

Uno LSP può appartenere a più di una categoria. Ad esempio, un firewall/LSP di sicurezza può appartenere alle categorie Inspector **( \_ controllo LSP**) e firewall **( \_ LSP firewall**).

Se uno LSP non dispone di un set di categorie, viene considerato nella categoria tutti gli altri. Questa categoria LSP non verrà caricata nei servizi o nei processi di sistema, ad esempio LSASS, Winlogon e molti processi svchost.

## <a name="categorizing-lsps"></a>Categorizzazione di LSP

In Windows Vista e versioni successive sono disponibili diverse nuove funzioni per la categorizzazione di un LSP:

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Per categorizzare un LSP, la funzione [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) o [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) viene chiamata con un GUID per identificare la voce nascosta LSP, la classe Information da impostare per questa voce del protocollo LSP e un set di flag usati per modificare il comportamento della funzione.

La funzione [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) o [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) viene usata in modo analogo per recuperare i dati associati a una classe di informazioni per uno LSP.

## <a name="categorizing-applications"></a>Categorizzazione di applicazioni

In Windows Vista e versioni successive sono disponibili diverse nuove funzioni per la categorizzazione di un'applicazione:

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Per categorizzare un'applicazione, la funzione [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) viene chiamata con il percorso di caricamento dell'immagine eseguibile per identificare l'applicazione, gli argomenti della riga di comando usati all'avvio dell'applicazione e le categorie LSP consentite per tutte le istanze dell'applicazione.

La funzione [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) viene usata in modo analogo per recuperare le categorie del provider di servizi a più livelli (LSP) associate a un'applicazione.

## <a name="determining-which-lsps-get-loaded"></a>Determinare quali LSP vengono caricati

La parte finale della categorizzazione di LSP consiste nel determinare quali lsp verranno caricati in quali processi. Quando un processo carica Winsock, vengono eseguiti i confronti seguenti tra la categoria dell'applicazione e le categorie LSP per tutti LSP installati:

-   Se l'applicazione non è categorizzata, consentire il caricamento di tutti i LSP nel processo.
-   Se per l'applicazione e il LSP sono state assegnate categorie, è necessario che siano soddisfatte tutte le condizioni seguenti: <dl> Almeno una delle categorie di LSP è presente nelle categorie specificate dell'applicazione.  
    Nelle categorie LSP vengono specificate solo le categorie specificate nelle categorie specificate dell'applicazione. Se, ad esempio, l'applicazione specifica una categoria, deve trovarsi nella categoria del LSP.  
    Se la \_ categoria di sistema LSP è presente nella categoria dell'applicazione, deve essere presente nelle categorie del LSP.  
    </dl>

> [!Note]  
> Se uno LSP non è categorizzato, la relativa categoria è effettivamente zero. Per trovare una corrispondenza, è necessario che tutte le categorie specificate di LSP siano presenti nelle categorie dell'applicazione (le categorie dell'applicazione devono essere un superset delle categorie di LSP) con l'avvertenza che se il \_ sistema LSP è presente nella categoria dell'applicazione, deve essere presente anche nella categoria del LSP.

 

Si consideri l'esempio seguente:

L'applicazione *Foo.exe* è categorizzata come LSP \_ System + LSP \_ Firewall + LSP \_ Crypto \_ Compress. Il *Bar.exe* di applicazione è categorizzato come LSP \_ Firewall + LSP \_ Crypto \_ Compress. Nel sistema sono installati quattro LSP:

-   LSP1 ha impostato una categoria di \_ sistema LSP.
-   LSP2 non è un set di categorie, quindi la relativa categoria è zero.
-   LSP3 ha impostato una categoria di \_ Firewall LSP.
-   LSP4 ha impostato categorie di LSP \_ System + LSP \_ Firewall + LSP \_ Crypto \_ Compress + LSP \_ Inspector

In questo esempio, l'applicazione *Foo.exe* CARICHERÀ solo LSP1, mentre l'applicazione *Bar.exe* caricherà LSP3.

## <a name="determining-winsock-providers-installed"></a>Determinazione del provider Winsock installato

Il Software Development Kit (SDK) di Microsoft Windows include un programma Winsock di esempio che può essere usato per determinare i provider di trasporto Winsock installati in un computer locale. Per impostazione predefinita, il codice sorgente per questo esempio Winsock è installato nella seguente directory del Windows SDK per Windows 7:

*C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ NetDs \\ Winsock \\ LSP*

Questo esempio è un'utilità per l'installazione e il test di provider di servizi a più livelli. Ma può anche essere usato per raccogliere informazioni dettagliate a livello di codice dal catalogo Winsock in un computer locale. Per elencare tutti i provider Winsock correnti, inclusi i provider di base e i provider di servizi del livello, compilare questo esempio Winsock ed eseguire il comando seguente della console:

**instlsp-p**

L'output sarà un elenco di provider Winsock installati nel computer locale, inclusi i provider di servizi a più livelli. L'output elenca l'ID del catalogo e il nome della stringa per il provider Winsock

Per raccogliere informazioni più dettagliate su tutti i provider Winsock, eseguire il comando seguente della console:

**instlsp-p-v**

L'output sarà un elenco di strutture di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) supportate nel computer locale.

Per un elenco di provider di servizi su più livelli installati nel computer locale, eseguire il comando seguente della console:

**instlsp-l**

Per eseguire il mapping della struttura LSP, eseguire il comando seguente della console:

**instlsp-m**

> [!Note]  
> La funzionalità TDI è deprecata e verrà rimossa nelle versioni future di Microsoft Windows. A seconda di come si usa TDI, usare il kernel Winsock (WSK) o Windows Filtering Platform (WFP). Per ulteriori informazioni su WFP e WSK, vedere [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md) e [Winsock Kernel](/windows-hardware/drivers/ddi/_netvista/). Per un intervento di Blog sulla rete di Windows Core su WSK e TDI, vedere [Introduzione al kernel Winsock (WSK)](/archive/blogs/wndp/).

 

 

 

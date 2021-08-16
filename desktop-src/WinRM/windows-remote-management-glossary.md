---
title: Windows Glossario della gestione remota
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532562a45090040cebbefae2bfff601727efb8bca794a9d9833e61a53ad63a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743266"
---
# <a name="windows-remote-management-glossary"></a>Windows Glossario della gestione remota


<dl> <dt>

wsman:Items****
</dt> <dd>

Elemento WS-Management di protocollo restituito in un'enumerazione che ottiene sia le istanze che le [*EPR dell'istanza*](/windows). **wsman:Items è** un contenitore che contiene un'istanza e la relativa EPR. Questo tipo di enumerazione viene avviato quando il flag **WSManFlagReturnObjectAndEPR** viene impostato nella richiesta.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**baseboard management controller (BMC)**
</dt> <dd>

Microcontroller collegato in locale a un server. I BBM hanno sensori che monitorano lo stato fisico del server e una connessione di rete separata in grado di comunicare in rete, anche se il server è offline. È possibile accedere ai dati BMC tramite il provider [*WMI IPMI (Intelligent Platform Management Interface).*](windows-remote-management-glossary.md)

</dd> <dt>

**Autenticazione di base**
</dt> <dd>

Nome utente e password inviati nello scambio di autenticazione. L'autenticazione di base può essere configurata per l'uso del trasporto HTTP o HTTPS in un dominio o in un gruppo di lavoro. Si tratta del metodo di autenticazione meno sicuro.

</dd> <dt>

**Baseboard Management Controller (BMC)**
</dt> <dd>

Vedere [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Cim**
</dt> <dd>

Vedere [*Common Information Model (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**Client**
</dt> <dd>

L'applicazione client che usa WS-Management protocollo per accedere al servizio di gestione sul computer locale o remoto.

</dd> <dt>

**Common Information Model (CIM)**
</dt> <dd>

Modello [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) che descrive come rappresentare oggetti computer e di rete reali. CIM utilizza un paradigma orientato agli oggetti, in cui gli oggetti gestiti vengono modellati mediante i concetti di classi e istanze.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Autenticazione del digest**
</dt> <dd>

Scambio in cui il server riceve una richiesta da un client e invia i dati relativi al client a un server di autenticazione, in genere un controller di dominio. Se il client è autenticato, il server riceve una chiave di sessione digest usata per autenticare le richieste successive dal client.

</dd> <dt>

**Distributed Management Task Force (DMTF)**
</dt> <dd>

Organizzazione del settore che sviluppa standard di gestione e tecnologia di integrazione per ambienti aziendali e Internet.

</dd> <dt>

**Dmtf**
</dt> <dd>

Vedere [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Endpoint**
</dt> <dd>

Risorsa che può essere indirizzata da un [*riferimento all'endpoint .*](windows-remote-management-glossary.md)

</dd> <dt>

**Riferimento all'endpoint (EPR)**
</dt> <dd>

Combinazione di WS-Addressing e WS-Management che insieme descrivono un indirizzo per una risorsa nell'intestazione SOAP del messaggio. Si tratta di un termine di servizio Web.

</dd> <dt>

**enumeration**
</dt> <dd>

Un set, o raccolta, di istanze [*di risorsa*](windows-remote-management-glossary.md) o l'azione di richiesta di tale set. Nel WS-Management, [*WS-Enumeration*](windows-remote-management-glossary.md) viene usato per ottenere la raccolta. Nell'implementazione di scripting del servizio WinRM dell'enumerazione vengono usati [**Session.Enumerate**](session-enumerate.md) e l'oggetto [**Enumerator.**](enumerator.md) Il metodo e l'interfaccia C++ corrispondenti [**sono IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) e [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

**EPR**
</dt> <dd>

Vedere [*Endpoint Reference (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**Servizio di raccolta eventi**
</dt> <dd>

Componente del sistema operativo che riceve eventi dal BMC e da altri componenti o applicazioni del sistema operativo.

</dd> <dt>

**inoltro di eventi**
</dt> <dd>

È possibile inviare una notifica degli eventi che si verificano nei computer remoti alle applicazioni di sottoscrizione. L'inoltro degli eventi non è una funzionalità di Gestione remota Windows, ma del [Windows eventi](/windows/desktop/WES/windows-event-log). L'inoltro degli eventi diventa disponibile per la prima volta in Windows Vista. Le applicazioni di gestione, ad esempio Microsoft Operations Manager (MOM), usano l'inoltro di eventi.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Meccanismo di query per specificare un set limitato di istanze nella richiesta di una [*risorsa*](windows-remote-management-glossary.md). È possibile specificare un *parametro di* filtro nelle chiamate [**a Session.Enumerate**](session-enumerate.md) o [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

**filtrare il dialetto**
</dt> <dd>

Stringa XML che identifica il dialetto XML utilizzato per specificare un filtro [*in*](windows-remote-management-glossary.md) una chiamata a [**Session.Enumerate**](session-enumerate.md) o [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate). Il servizio Gestione remota Windows supporta [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) come dialetto di filtro quando si ricevono richieste.

</dd> <dt>

**Frammento**
</dt> <dd>

Stringa XML che identifica parte di un'istanza di una risorsa anziché l'intera risorsa. Il supporto dei frammenti è disponibile [**nell'oggetto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**dialetto frammento**
</dt> <dd>

Stringa XML che identifica il dialetto XML utilizzato per specificare un [*frammento*](windows-remote-management-glossary.md). Il supporto dei frammenti è disponibile [**nell'oggetto ResourceLocator.**](resourcelocator.md) Il servizio Gestione remota Windows supporta [*XPath*](windows-remote-management-glossary.md) per il dialetto dei frammenti durante la ricezione delle richieste.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**in-band**
</dt> <dd>

L'applicazione client ottiene i dati BMC tramite il [*listener*](windows-remote-management-glossary.md) WinRM nel sistema operativo.

</dd> <dt>

**IpMI (Intelligent Platform Management Interface)**
</dt> <dd>

Standard del settore IT per l'architettura del controller di gestione della [*baseboard (BMC).*](windows-remote-management-glossary.md) Le Windows di gestione hardware forniscono un [*driver IPMI*](windows-remote-management-glossary.md) e un [*provider IPMI*](windows-remote-management-glossary.md) WMI che consentono agli script di gestione, agli strumenti da riga di comando e alle applicazioni di ottenere dati BMC. Il provider IPMI dispone di [classi](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI .

</dd> <dt>

**IPMI**
</dt> <dd>

Vedere [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Driver IPMI**
</dt> <dd>

Driver del kernel che consente l'accesso [*ai dispositivi BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) dai componenti del sistema operativo.

</dd> <dt>

**Provider IPMI**
</dt> <dd>

Provider WMI standard che definisce le classi che modellano [*l'IPMI*](windows-remote-management-glossary.md) e i relativi dati. Il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) è una DLL COM che ottiene dati dal BMC.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Kcs**
</dt> <dd>

Vedere [*Stile del controller della tastiera (KCS).*](windows-remote-management-glossary.md)

</dd> <dt>

**Autenticazione Kerberos**
</dt> <dd>

Metodo di autenticazione reciproca tra il client e il server che usa chiavi crittografate. Per i computer in esecuzione Windows sistema operativo basato su , l'account client deve essere un account di dominio nello stesso dominio del server. Quando un client usa le credenziali predefinite, Kerberos è il metodo di autenticazione se la stringa di connessione non è una delle seguenti: localhost, 127.0.0.1 o \[ ::1 \] .

</dd> <dt>

**Stile controller tastiera (KCS)**
</dt> <dd>

Protocollo usato dal [*driver IPMI per*](windows-remote-management-glossary.md) comunicare con il controller di gestione della [*baseboard (BMC).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Servizio di gestione che implementa WS-Management protocollo per inviare e ricevere messaggi. WinRM è un servizio listener. Un listener è definito da un trasporto (HTTP o HTTPS) e da un indirizzo IPv4 o IPv6. È possibile creare più di un'istanza del listener WinRM in un singolo computer fornendo loro un indirizzo TCP/IP o un numero di porta diverso.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

Pacchetto di informazioni trasmesse tra computer o reti separate costruite con il [*protocollo*](windows-remote-management-glossary.md) SOAP. Il pacchetto ha un'intestazione che descrive la destinazione e il trasporto del messaggio e un corpo che contiene il contenuto da utilizzare all'arrivo del messaggio. Un messaggio è una combinazione di elementi di specifiche quali [*WS-Addressing,*](windows-remote-management-glossary.md) [*WS-Transfer*](windows-remote-management-glossary.md)e [*WS-Management.*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**Namespace**
</dt> <dd>

Uno spazio dei nomi [*WMI,*](windows-remote-management-glossary.md) ovvero un raggruppamento logico di classi e istanze WMI per controllare l'ambito e l'accesso. L'origine più frequente dei dati di gestione per i sistemi che eseguono Windows è lo spazio dei nomi radice cimv2, che contiene classi come \\ [**Win32 \_ Process.**](/windows/desktop/CIMWin32Prov/win32-process) Gli spazi dei nomi vengono visualizzati nell'URI della risorsa per le classi WMI, ad esempio https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .

</dd> <dt>

**Negoziazione dell'autenticazione**
</dt> <dd>

Tipo di autenticazione Single Sign-On negoziato che rappresenta l'implementazione Windows semplice e protetta del meccanismo di negoziazione [*GSSAPI (SPNEGO).*](windows-remote-management-glossary.md) La negoziazione SPNEGO determina se l'autenticazione viene gestita da Kerberos o NTLM. Kerberos è il meccanismo preferito. L'autenticazione negoziata Windows sistemi basati su certificati è detta anche autenticazione Windows integrata.

</dd> <dt>

**sensore numerico**
</dt> <dd>

Tipo numerico di sensore in un [*baseboard management controller (BMC),*](windows-remote-management-glossary.md)ad esempio temperatura o tensione.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**opzione**
</dt> <dd>

Dati aggiuntivi richiesti dal provider di risorse per elaborare una richiesta. Ad esempio, alcuni provider WMI richiedono dati aggiuntivi forniti come [**oggetti IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet.**](/windows/desktop/WmiSdk/swbemnamedvalueset) Il supporto delle opzioni è disponibile [**nell'oggetto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**fuori banda**
</dt> <dd>

L'applicazione client ottiene i dati direttamente dal [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) di un altro computer, anziché tramite il [*listener*](windows-remote-management-glossary.md) WinRM nel sistema operativo.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Tirare**
</dt> <dd>

Viene inviato un messaggio pull [*WS-Enumeration*](windows-remote-management-glossary.md) per continuare un'enumerazione avviata da una chiamata iniziale a WS-Enumeration:Enumerate. L'operazione pull nel servizio Gestione remota Windows viene eseguita da [**Enumerator.ReadItem**](enumerator-readitem.md) o [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**Risorsa**
</dt> <dd>

Endpoint [*che*](windows-remote-management-glossary.md) rappresenta un tipo distinto di operazione o valore di gestione. Un servizio espone una o più risorse e alcune risorse possono avere più di un'istanza. Una risorsa di gestione è simile a una classe WMI o a una tabella di database e un'istanza è simile a un'istanza della classe o di una riga nella tabella. Ad esempio, la [**classe \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) rappresenta una risorsa. `Win32_LogicalDisk="C:\"` è un'istanza specifica della risorsa.

</dd> <dt>

**URI risorsa**
</dt> <dd>

URI [*(Uniform Resource Identifier)*](windows-remote-management-glossary.md) usato per identificare un tipo specifico di risorsa, ad esempio dischi o processi, in un sistema.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Sel**
</dt> <dd>

Vedere [*Registro eventi di sistema (SEL).*](windows-remote-management-glossary.md)

</dd> <dt>

**Adattatore SEL**
</dt> <dd>

Adattatore che invia i dati del controller di gestione della [*baseboard (BMC)*](windows-remote-management-glossary.md) all'agente [*di raccolta eventi*](windows-remote-management-glossary.md).

</dd> <dt>

**selector**
</dt> <dd>

Coppia nome/valore che rappresenta una particolare istanza di una [*risorsa*](windows-remote-management-glossary.md). Si tratta essenzialmente di un filtro o di una "chiave" che identifica l'istanza desiderata della risorsa. Il supporto del selettore è disponibile [**nell'oggetto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**Sensore**
</dt> <dd>

Un dispositivo di misurazione in [*un baseboard management controller (BMC).*](windows-remote-management-glossary.md)

</dd> <dt>

**Servizio**
</dt> <dd>

Applicazione che fornisce servizi di gestione ai client tramite il protocollo WS-Management e altri [*servizi Web*](windows-remote-management-glossary.md). Un servizio è in genere uguale al [*listener*](windows-remote-management-glossary.md) in una rete. Il servizio ha un indirizzo di trasporto fisico.

</dd> <dt>

**Sessione**
</dt> <dd>

Una connessione tra un Windows [*client*](windows-remote-management-glossary.md) di gestione remota e il listener o il [*servizio*](windows-remote-management-glossary.md)Gestione remota Windows locale o remoto. Questa connessione è simile alla connessione tra uno script client WMI e WMI in un server remoto. Le operazioni di sessione, ad esempio l'enumerazione di una risorsa (Enumerate), il recupero di un'istanza di una risorsa (Get) o l'esecuzione di un metodo di risorsa (Invoke) sono metodi **dell'oggetto Session.** Un **oggetto Session** viene creato da [**WSMan.CreateSession.**](wsman-createsession.md)

</dd> <dt>

**Meccanismo di negoziazione GSS-API semplice e protetto (SPNEGO)**
</dt> <dd>

Meccanismo di autenticazione usato dal client o dal server che riceve le richieste di dati tramite WinRM in un contesto di Active Directory. SPNEGO si basa su un protocollo REQUEST FOR COMMENTS (RFC) prodotto da Internet Engineering Task Force (IETF). SPNEGO è noto anche come [*Windows integrata*](windows-remote-management-glossary.md)di , il termine usato negli argomenti della Guida Windows gestione remota.

</dd> <dt>

**Simple Object Access Protocol (SOAP)**
</dt> <dd>

Protocollo basato su XML utilizzato dai servizi Web.

</dd> <dt>

**Sapone**
</dt> <dd>

Vedere [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).

</dd> <dt>

**Spnego**
</dt> <dd>

Vedere [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO) (Meccanismo*](windows-remote-management-glossary.md)di negoziazione GSS-API semplice e protetto ).

</dd> <dt>

**Registro eventi di sistema (SEL)**
</dt> <dd>

Database di eventi nell'hardware del controller di gestione [*della baseboard ( BMC).*](windows-remote-management-glossary.md) [*L'adapter SEL*](windows-remote-management-glossary.md) trasmette questi eventi al sistema operativo.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**URI (Uniform Resource Identifier)**
</dt> <dd>

Stringa che identifica una risorsa nell'organizzazione, ad esempio un computer, un processo, un'unità disco o un sensore di temperatura in un [*baseboard management controller (BMC).*](windows-remote-management-glossary.md) L'URI è il meccanismo di indirizzamento del servizio Web definito in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): Sintassi generica \[ RFC3986. \]

</dd> <dt>

**URI**
</dt> <dd>

Vedere [*URI (Uniform Resource Identifier).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**servizio Web**
</dt> <dd>

Un'applicazione software usata per l'interazione tra computer in Internet o in una rete. I servizi Web sono descritti dal [*linguaggio WSDL (Web Service Description Language).*](windows-remote-management-glossary.md) La descrizione specifica del servizio Web indica ad altri servizi come interagire con il servizio Web tramite messaggi SOAP. I messaggi vengono trasmessi tra computer da un trasporto, in genere HTTP o HTTPS. [*WS-Addressing,*](windows-remote-management-glossary.md) [*WS-Eventing*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md) sono esempi di protocolli usati dalle applicazioni del servizio Web per comunicare tra loro.

</dd> <dt>

**Wsdl (Web Service Description Language)**
</dt> <dd>

Linguaggio basato su XML utilizzato per definire la modalità di interazione con un servizio Web. In genere, wsdl descrive i messaggi SOAP necessari al servizio Web per restituire dati o eseguire operazioni. Wsdl consente a un'implementazione da un sistema operativo di comunicare con il servizio Web implementato in un altro sistema operativo, purché siano soddisfatti i requisiti del wsdl.

</dd> <dt>

**Autenticazione integrata di Windows**
</dt> <dd>

Vedere [*Negoziazione dell'autenticazione.*](windows-remote-management-glossary.md)

</dd> <dt>

**Strumentazione gestione Windows (WMI)**
</dt> <dd>

Implementazione Microsoft dello standard Web-Based Enterprise Management (WBEM) pubblicato da [*Distributed Management Task Force (DMTF).*](windows-remote-management-glossary.md) WMI consente di gestire computer locali e remoti e modella oggetti computer e di rete usando un'estensione dello standard [*Common Information Model (CIM).*](windows-remote-management-glossary.md)

</dd> <dt>

**Gestione remota Windows (WinRM)**
</dt> <dd>

Implementazione Microsoft di un servizio Web di gestione basato sul protocollo [*WS-Management*](windows-remote-management-glossary.md) standard pubblico.

</dd> <dt>

**Windows Remote Shell (WinRS)**
</dt> <dd>

Uno strumento shell che si basa Windows [*gestione remota*](windows-remote-management-glossary.md) per eseguire comandi remoti, in particolare per i server headless. Lo strumento da riga di comando è Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Vedere [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Plug-in WMI**
</dt> <dd>

Plug-in WinRM che rende disponibili i dati WMI per i client WinRM.

</dd> <dt>

**WS-Addressing (wsa)**
</dt> <dd>

Protocollo standard pubblico, basato su SOAP, che crea un sistema di indirizzamento utilizzato nelle intestazioni dei messaggi inviati su Internet. Lo standard definisce la modalità di posizione delle risorse tra reti e firewall. WS-Addressing è uno dei protocolli del servizio Web che costituiscono il WS-Management protocollo.

</dd> <dt>

**Enumerazione WS (wsen)**
</dt> <dd>

Protocollo standard pubblico, basato su SOAP, per enumerare una sequenza di elementi XML che possono rappresentare raccolte di dati, log o altre strutture di informazioni lineari. WS-Enumeration è uno dei protocolli del servizio Web che costituiscono il WS-Management protocollo.

</dd> <dt>

**WS-Eventing (wse)**
</dt> <dd>

Protocollo standard pubblico, basato su SOAP, che consente a un servizio Web (sottoscrittore) di sottoscrivere e accettare messaggi di notifica degli eventi da un altro servizio Web (origine evento). WS-Eventing è uno dei protocolli del servizio Web che costituiscono il WS-Management protocollo.

</dd> <dt>

**WS-Management**
</dt> <dd>

Protocollo standard pubblico, basato su SOAP, per la condivisione dei dati di gestione tra tutti i sistemi operativi, i computer e i dispositivi. Tutti [*i messaggi*](windows-remote-management-glossary.md) inviati dai componenti client o server WinRM usano questo protocollo.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Protocollo standard pubblico, basato su SOAP, per accedere alle rappresentazioni XML delle risorse basate su servizi Web tramite un semplice set di verbi, ad esempio Get, Put, Invoke o Delete. WS-Transfer definisce le operazioni per l'invio e la ricezione della rappresentazione di una determinata risorsa e delle operazioni per la creazione o l'eliminazione di una risorsa e della relativa rappresentazione corrispondente.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Notazione di percorso per l'indirizzamento di parti di un documento XML, simile a un URL. Un'espressione XPath è una sequenza di frasi da ottenere dalla posizione corrente nel documento XML a un altro nodo o set di nodi. Le frasi sono separate da caratteri barra ("/"). Il servizio Gestione remota Windows supporta [XPath per](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) il [*dialetto frammento*](windows-remote-management-glossary.md).

</dd> </dl>

 

 
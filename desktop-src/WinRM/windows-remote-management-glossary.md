---
title: Glossario Gestione remota Windows
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321093"
---
# <a name="windows-remote-management-glossary"></a>Glossario Gestione remota Windows


<dl> <dt>

WSMan: elementi * * * *
</dt> <dd>

Un WS-Management elemento del protocollo restituito in un'enumerazione che ottiene sia le istanze di che l'istanza di [*EPRs*](/windows). **WSMan: gli elementi** sono un contenitore che include un'istanza di e il relativo EPR. Questo tipo di enumerazione viene avviato quando il flag **WSManFlagReturnObjectAndEPR** viene impostato nella richiesta.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**Baseboard Management Controller (BMC)**
</dt> <dd>

Un microcontroller collegato localmente a un server. BMC hanno sensori che monitorano lo stato fisico del server e una connessione di rete separata in grado di comunicare in rete, anche se il server è offline. È possibile accedere ai dati BMC tramite il provider WMI [*IPMI (Intelligent Platform Management Interface)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Autenticazione di base**
</dt> <dd>

Nome utente e password inviati nello scambio di autenticazione. L'autenticazione di base può essere configurata in modo da utilizzare il trasporto HTTP o HTTPS in un dominio o un gruppo di lavoro. Si tratta del metodo di autenticazione meno sicuro.

</dd> <dt>

**Baseboard Management Controller (BMC)**
</dt> <dd>

Vedere [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**CIM**
</dt> <dd>

Vedere [*Common Information Model (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Applicazione client che utilizza il protocollo WS-Management per accedere al servizio di gestione nel computer locale o remoto.

</dd> <dt>

**Common Information Model (CIM)**
</dt> <dd>

Modello [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) che descrive come rappresentare oggetti di rete e computer reali. CIM utilizza un paradigma orientato agli oggetti, in cui gli oggetti gestiti vengono modellati mediante i concetti di classi e istanze.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Autenticazione del digest**
</dt> <dd>

Uno scambio in cui il server riceve una richiesta da un client e invia i dati sul client a un server di autenticazione, in genere un controller di dominio. Se il client viene autenticato, il server riceve una chiave di sessione digest utilizzata per autenticare le richieste successive dal client.

</dd> <dt>

**Distributed Management Task Force (DMTF)**
</dt> <dd>

Organizzazione del settore che sviluppa gli standard di gestione e la tecnologia di integrazione per ambienti aziendali e Internet.

</dd> <dt>

**DMTF**
</dt> <dd>

Vedere [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**endpoint**
</dt> <dd>

Risorsa che può essere risolta da un [*riferimento all'endpoint (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**riferimento endpoint (EPR)**
</dt> <dd>

Combinazione di WS-Addressing e WS-Management che indirizzano elementi che insieme descrivono un indirizzo per una risorsa nell'intestazione SOAP del messaggio. Si tratta di un termine di servizio Web.

</dd> <dt>

**enumeration**
</dt> <dd>

Set, o raccolta, di istanze di [*risorse*](windows-remote-management-glossary.md) o dell'azione di richiesta di tale set. In WS-Management protocollo, per ottenere la raccolta viene usato [*WS-Enumeration*](windows-remote-management-glossary.md) . Nell'implementazione di scripting del servizio WinRM di Enumeration vengono usati [**Session. enumerate**](session-enumerate.md) e l'oggetto [**enumeratore**](enumerator.md) . Il metodo e l'interfaccia C++ corrispondenti sono [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) e [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

**EPR**
</dt> <dd>

Vedere [*riferimento endpoint (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**Servizio raccolta eventi**
</dt> <dd>

Componente del sistema operativo che riceve gli eventi dal BMC e da altri componenti o applicazioni del sistema operativo.

</dd> <dt>

**invio di eventi**
</dt> <dd>

Una notifica degli eventi che si verificano in computer remoti può essere inviata alle applicazioni di sottoscrizione. L'invio di eventi non è una funzionalità di WinRM, ma del [registro eventi di Windows](/windows/desktop/WES/windows-event-log). L'invio di eventi diventa disponibile per la prima volta in Windows Vista. Le applicazioni di gestione, ad esempio Microsoft Operations Manager (MOM) usano l'invio di eventi.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Meccanismo di query per specificare un set limitato di istanze nella richiesta di una [*risorsa*](windows-remote-management-glossary.md). È possibile specificare un parametro di *filtro* per le chiamate a [**Session. enumerate**](session-enumerate.md) o [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

**dialetto filtro**
</dt> <dd>

Stringa XML che identifica il dialetto XML utilizzato per specificare un [*filtro*](windows-remote-management-glossary.md) in una chiamata a [**Session. enumerate**](session-enumerate.md) o [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate). Il servizio gestione remota Windows supporta [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) come dialetto di filtro durante la ricezione di richieste.

</dd> <dt>

**frammento**
</dt> <dd>

Stringa XML che identifica parte di un'istanza di una risorsa anziché l'intera risorsa. Il supporto del frammento è disponibile nell'oggetto [**resourceLocator**](resourcelocator.md) .

</dd> <dt>

**dialetto frammento**
</dt> <dd>

Stringa XML che identifica il dialetto XML utilizzato per specificare un [*frammento*](windows-remote-management-glossary.md). Il supporto del frammento è disponibile nell'oggetto [**resourceLocator**](resourcelocator.md) . Il servizio WinRM supporta [*XPath*](windows-remote-management-glossary.md) per il dialetto Fragment durante la ricezione di richieste.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**in banda**
</dt> <dd>

L'applicazione client ottiene i dati BMC tramite il [*listener*](windows-remote-management-glossary.md) WinRM nel sistema operativo.

</dd> <dt>

**Interfaccia di gestione piattaforma intelligente (IPMI)**
</dt> <dd>

Standard del settore IT per l'architettura di [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md). Le funzionalità di gestione hardware di Windows forniscono un [*driver IPMI*](windows-remote-management-glossary.md) e un [*provider IPMI*](windows-remote-management-glossary.md) WMI che consentono di ottenere dati BMC tramite script di gestione, strumenti da riga di comando e applicazioni. Il provider IPMI dispone di [classi](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.

</dd> <dt>

**IPMI**
</dt> <dd>

Vedere [*Intelligent Platform Management Interface (impi)*](windows-remote-management-glossary.md).

</dd> <dt>

**Driver IPMI**
</dt> <dd>

Driver del kernel che consente di accedere ai dispositivi [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) dai componenti del sistema operativo.

</dd> <dt>

**Provider IPMI**
</dt> <dd>

Provider WMI standard che definisce le classi che modellano l' [*IPMI*](windows-remote-management-glossary.md) e i relativi dati. Il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) è una DLL COM che ottiene i dati dal BMC.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**KCS**
</dt> <dd>

Vedere [*stile del controller della tastiera (KCS)*](windows-remote-management-glossary.md).

</dd> <dt>

**Autenticazione Kerberos**
</dt> <dd>

Metodo di autenticazione reciproca tra il client e il server che utilizza chiavi crittografate. Per i computer in cui è in esecuzione un sistema operativo basato su Windows, l'account client deve essere un account di dominio nello stesso dominio del server. Quando un client utilizza credenziali predefinite, Kerberos è il metodo di autenticazione se la stringa di connessione non è una delle seguenti: localhost, 127.0.0.1 o \[ :: 1 \] .

</dd> <dt>

**Stile del controller della tastiera (KCS)**
</dt> <dd>

Il protocollo usato dal [*driver IPMI*](windows-remote-management-glossary.md) per comunicare con il [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Un servizio di gestione che implementa WS-Management protocollo per inviare e ricevere messaggi. WinRM è un servizio di listener. Un listener viene definito da un trasporto (HTTP o HTTPS) e da un indirizzo IPv4 o IPv6. È possibile creare più di un'istanza del listener WinRM in un singolo computer assegnando loro un indirizzo TCP/IP o un numero di porta diverso.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

Un pacchetto di informazioni trasmesse tra computer o reti separate costruite con il protocollo [*SOAP*](windows-remote-management-glossary.md) . Nel pacchetto è presente un'intestazione che descrive la destinazione e il trasporto del messaggio e un corpo che contiene il contenuto da utilizzare all'arrivo del messaggio. Un messaggio è costituito da una combinazione di elementi di specifiche quali [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Uno spazio dei nomi [*WMI*](windows-remote-management-glossary.md) , ovvero un raggruppamento logico di classi e istanze WMI per controllare l'ambito e l'accesso. L'origine dei dati di gestione più frequente per i sistemi che eseguono Windows è lo \\ spazio dei nomi CIMV2 radice, che contiene classi come il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process). Gli spazi dei nomi vengono visualizzati nell'URI della risorsa per le classi WMI, ad esempio https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .

</dd> <dt>

**Negozia autenticazione**
</dt> <dd>

Tipo di autenticazione negoziato e Single Sign-on che rappresenta l'implementazione di Windows del [*meccanismo di negoziazione GSSAPI semplice e protetto (SPNEGO)*](windows-remote-management-glossary.md). La negoziazione SPNEGO determina se l'autenticazione è gestita da Kerberos o NTLM. Kerberos è il meccanismo preferito. L'autenticazione Negotiate nei sistemi basati su Windows è detta anche autenticazione integrata di Windows.

</dd> <dt>

**sensore numerico**
</dt> <dd>

Tipo numerico di sensore in un [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md), ad esempio temperatura o tensione.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**opzione**
</dt> <dd>

Dati aggiuntivi richiesti dal provider di risorse per elaborare una richiesta. Alcuni provider WMI, ad esempio, richiedono dati aggiuntivi forniti come oggetti [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) . Il supporto dell'opzione è disponibile nell'oggetto [**resourceLocator**](resourcelocator.md) .

</dd> <dt>

**fuori banda**
</dt> <dd>

L'applicazione client ottiene i dati direttamente dal [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) di un altro computer, anziché tramite il [*listener*](windows-remote-management-glossary.md) WinRM nel sistema operativo.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**tirare**
</dt> <dd>

Viene inviato un messaggio pull [*WS-Enumeration*](windows-remote-management-glossary.md) per continuare un'enumerazione avviata da una chiamata iniziale a WS-Enumeration: enumerate. L'operazione pull nel servizio gestione remota Windows viene eseguita da [**Enumerator. ReadItem**](enumerator-readitem.md) o [**IWSManEnumerator:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**risorse**
</dt> <dd>

[*Endpoint*](windows-remote-management-glossary.md) che rappresenta un tipo distinto di operazione di gestione o valore. Un servizio espone una o più risorse e alcune risorse possono avere più di un'istanza. Una risorsa di gestione è simile a una classe WMI o a una tabella di database e un'istanza è simile a un'istanza della classe o a una riga nella tabella. Ad esempio, la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) rappresenta una risorsa. `Win32_LogicalDisk="C:\"` è un'istanza specifica della risorsa.

</dd> <dt>

**URI risorsa**
</dt> <dd>

[*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) usato per identificare un tipo specifico di risorsa, ad esempio i dischi o i processi, in un sistema.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**SEL**
</dt> <dd>

Vedere [*registro eventi di sistema (SEL)*](windows-remote-management-glossary.md).

</dd> <dt>

**Adapter SEL**
</dt> <dd>

Adapter che invia i dati di [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) all' [*agente di raccolta eventi*](windows-remote-management-glossary.md).

</dd> <dt>

**selector**
</dt> <dd>

Coppia di nome e valore che rappresenta una particolare istanza di una [*risorsa*](windows-remote-management-glossary.md). Si tratta essenzialmente di un filtro o di una "chiave" che identifica l'istanza desiderata della risorsa. Il supporto del selettore si trova nell'oggetto [**resourceLocator**](resourcelocator.md) .

</dd> <dt>

**sensore**
</dt> <dd>

Un dispositivo di misurazione in un [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).

</dd> <dt>

**servizio**
</dt> <dd>

Applicazione che fornisce servizi di gestione ai client tramite il protocollo WS-Management e altri [*servizi Web*](windows-remote-management-glossary.md). Un servizio è in genere lo stesso del [*listener*](windows-remote-management-glossary.md) in una rete. Il servizio dispone di un indirizzo di trasporto fisico.

</dd> <dt>

**sessione**
</dt> <dd>

Connessione tra un [*client*](windows-remote-management-glossary.md) gestione remota Windows e il [*listener*](windows-remote-management-glossary.md)WinRM locale o remoto oppure il servizio. Questa connessione è simile alla connessione tra uno script client WMI e WMI in un server remoto. Le operazioni di sessione, ad esempio l'enumerazione di una risorsa (enumerazione), il recupero di un'istanza di una risorsa (Get) o l'esecuzione di un metodo di risorsa (Invoke) sono metodi dell'oggetto **Session** . Un oggetto **sessione** viene creato da [**WSMan. CreateSession**](wsman-createsession.md).

</dd> <dt>

**Simple and Protected GSS-meccanismo di negoziazione API (SPNEGO)**
</dt> <dd>

Meccanismo di autenticazione utilizzato dal client o dal server che riceve le richieste di dati tramite WinRM in un contesto di Active Directory. SPNEGO si basa su un protocollo RFC (Request for Comments) prodotto da Internet Engineering Task Force (IETF). SPNEGO è anche noto come [*autenticazione integrata di Windows*](windows-remote-management-glossary.md), il termine usato negli argomenti della guida Gestione remota Windows.

</dd> <dt>

**Simple Object Access Protocol (SOAP)**
</dt> <dd>

Protocollo basato su XML utilizzato dai servizi Web.

</dd> <dt>

**SOAP**
</dt> <dd>

Vedere [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).

</dd> <dt>

**SPNEGO**
</dt> <dd>

Vedere la pagina relativa al [*meccanismo di negoziazione API (SPNEGO) semplice e protetto*](windows-remote-management-glossary.md).

</dd> <dt>

**Registro eventi di sistema (SEL)**
</dt> <dd>

Database di eventi nell'hardware [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) . L' [*Adapter SEL*](windows-remote-management-glossary.md) trasmette questi eventi al sistema operativo.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Uniform Resource Identifier (URI)**
</dt> <dd>

Stringa che identifica una risorsa nell'azienda, ad esempio un computer, un processo, un'unità disco o un sensore di temperatura in un [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md). L'URI è il meccanismo di indirizzamento dei servizi Web definito in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): sintassi generica \[ RFC3986 \] .

</dd> <dt>

**URI**
</dt> <dd>

Vedere [*Uniform Resource Identifier (URI)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**servizio Web**
</dt> <dd>

Applicazione software utilizzata per l'interazione tra computer in Internet o in una rete. I servizi Web sono descritti da [*WSDL (Web Service Description Language)*](windows-remote-management-glossary.md). La descrizione specifica del servizio Web indica ad altri servizi come interagire con il servizio Web utilizzando messaggi SOAP. I messaggi vengono trasmessi tra computer da un trasporto, in genere HTTP o HTTPS. [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md) sono esempi di protocolli utilizzati dalle applicazioni del servizio Web per comunicare tra loro.

</dd> <dt>

**WSDL (Web Service Description Language)**
</dt> <dd>

Linguaggio basato su XML utilizzato per definire la modalità di interazione con un servizio Web. In genere, WSDL descrive i messaggi SOAP richiesti dal servizio Web per restituire i dati o eseguire operazioni. WSDL consente a un'implementazione di un sistema operativo di comunicare con il servizio Web implementato in un altro sistema operativo, purché siano soddisfatti i requisiti del documento WSDL.

</dd> <dt>

**Autenticazione integrata di Windows**
</dt> <dd>

Vedere [*Negotiate Authentication*](windows-remote-management-glossary.md).

</dd> <dt>

**Strumentazione gestione Windows (WMI)**
</dt> <dd>

Implementazione Microsoft dello standard WBEM (Web-Based Enterprise Management) pubblicata da [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md). WMI consente di gestire computer locali e remoti e di modellare oggetti computer e di rete utilizzando un'estensione dello standard [*Common Information Model (CIM)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Gestione remota Windows (WinRM)**
</dt> <dd>

Implementazione Microsoft di un servizio Web di gestione basato sul protocollo [*WS-Management*](windows-remote-management-glossary.md) pubblico standard.

</dd> <dt>

**Shell remota Windows (WinRS)**
</dt> <dd>

Uno strumento della shell che si basa su [*gestione remota Windows*](windows-remote-management-glossary.md) per eseguire comandi remoti, specialmente per i server Head. Lo strumento da riga di comando è Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Vedere [*Strumentazione gestione Windows (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Plug-in WMI**
</dt> <dd>

Il plug-in WinRM che rende disponibili i dati WMI ai client WinRM.

</dd> <dt>

**WS-Addressing (WSA)**
</dt> <dd>

Protocollo standard pubblico, che è basato su SOAP, che consente di creare un sistema di indirizzamento utilizzato nelle intestazioni dei messaggi inviati attraverso Internet. Lo standard definisce il modo in cui le risorse possono essere posizionate tra le reti e i firewall. WS-Addressing è uno dei protocolli del servizio Web che compongono il protocollo di WS-Management.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Protocollo standard pubblico, che è basato su SOAP, per l'enumerazione di una sequenza di elementi XML che possono rappresentare raccolte di dati, log o altre strutture di informazioni lineari. WS-Enumeration è uno dei protocolli del servizio Web che compongono il protocollo di WS-Management.

</dd> <dt>

**WS-Eventing (WSE)**
</dt> <dd>

Protocollo standard pubblico, che è basato su SOAP, che consente a un servizio Web (Sottoscrittore) di sottoscrivere e accettare messaggi di notifica degli eventi da un altro servizio Web (origine evento). WS-Eventing è uno dei protocolli del servizio Web che compongono il protocollo di WS-Management.

</dd> <dt>

**WS-Management**
</dt> <dd>

Protocollo standard pubblico, che è basato su SOAP, per la condivisione di dati di gestione tra tutti i sistemi operativi, i computer e i dispositivi. Tutti [*i messaggi*](windows-remote-management-glossary.md) inviati dal client o dai componenti del server WinRM utilizzano questo protocollo.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Protocollo standard pubblico, che è basato su SOAP, per l'accesso alle rappresentazioni XML di risorse basate su servizi Web tramite un semplice set di verbi come Get, put, Invoke o DELETE. WS-Transfer definisce le operazioni per l'invio e la ricezione della rappresentazione di una determinata risorsa e operazioni per la creazione o l'eliminazione di una risorsa e la relativa rappresentazione corrispondente.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Notazione di percorso per l'indirizzamento di parti di un documento XML, in modo analogo a un URL. Un'espressione XPath è una sequenza di frasi da ottenere dalla posizione corrente nel documento XML a un altro nodo o a un set di nodi. Le frasi sono separate da caratteri di barra ("/"). Il servizio WinRM supporta [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) per il [*dialetto del frammento*](windows-remote-management-glossary.md).

</dd> </dl>

 

 
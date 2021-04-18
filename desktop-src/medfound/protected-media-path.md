---
description: 'Questo argomento illustra tre argomenti correlati: ambiente protetto, gateway di interoperabilità multimediale, revoca e rinnovo.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Percorso supporto protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7304edadf1623d41bc2f1f5c6b2b4cda2dd5f598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104562673"
---
# <a name="protected-media-path"></a>Percorso supporto protetto

Questo argomento illustra tre argomenti correlati: ambiente protetto, gateway di interoperabilità multimediale, revoca e rinnovo.

-   Un ambiente protetto (PE) è un set di tecnologie che consente il flusso di contenuti protetti da e verso Windows Vista in modo protetto. Tutti i componenti all'interno di un ambiente protetto sono attendibili e il processo viene protetto da eventuali manomissioni.
-   Il percorso multimediale protetto (PMP) è un eseguibile che viene eseguito in un ambiente protetto.
-   Se un componente attendibile nel PE viene compromesso, dopo la scadenza del processo verrà revocato. Tuttavia, Microsoft fornisce un meccanismo di rinnovo per l'installazione di una versione attendibile più recente del componente, quando ne diventa disponibile uno.

Per informazioni sui componenti multimediali protetti per la firma del codice, vedere la white paper [firma del codice per i componenti multimediali protetti in Windows Vista](/windows-hardware/test/hlk/).

In questo argomento sono incluse le sezioni seguenti:

-   [Ambiente protetto](#protected-environment)
-   [Progettazione dell'ambiente protetto](#design-of-the-protected-environment)
-   [Percorso supporto protetto](#protected-media-path)
    -   [Autorità di attendibilità di input](#input-trust-authorities)
    -   [Autorità di attendibilità di output](#output-trust-authorities)
    -   [Oggetti Criteri](#policy-objects)
    -   [Creazione di oggetti in PMP](#creating-objects-in-the-pmp)
-   [Panoramica della negoziazione dei criteri](#overview-of-policy-negotiation)
-   [Revoca e rinnovo](#revocation-and-renewal)
-   [Protezione del collegamento di output](#output-link-protection)
-   [Argomenti correlati](#related-topics)

## <a name="protected-environment"></a>Ambiente protetto

La protezione del contenuto include più tecnologie, ciascuna delle quali tenta di garantire che il contenuto non possa essere utilizzato in modo non coerente con lo scopo del proprietario o del provider del contenuto. Queste tecnologie includono protezione da copia, protezione dei collegamenti, accesso condizionale e Digital Rights Management (DRM). La base di ogni è attendibilità: l'accesso al contenuto viene concesso solo ai componenti software che rispettano le condizioni per l'utilizzo assegnate a tale contenuto.

Per ridurre al minimo le minacce dal contenuto protetto, Windows Vista e il software Media Foundation consentono l'esecuzione di codice attendibile in un ambiente protetto. Un PE è un set di componenti, linee guida e strumenti progettati per migliorare la protezione contro la pirateria del contenuto.

Prima di esaminare il PE in modo più accurato, è importante comprendere le minacce che è stato progettato per ridurre al minimo. Si supponga di eseguire un'applicazione multimediale in un processo in modalità utente. L'applicazione è collegata alle varie librerie di collegamento dinamico (dll) che contengono plug-in multimediali, ad esempio i decodificatori. Anche altri processi vengono eseguiti in modalità utente e i vari driver vengono caricati nel kernel. Se non è presente alcun meccanismo di attendibilità, si verificano le minacce seguenti:

-   L'applicazione può accedere direttamente ai supporti protetti o hackerare la memoria del processo.
-   I plug-in possono accedere direttamente al contenuto o hackerare la memoria del processo.
-   Altri processi possono hackerare la memoria del processo multimediale direttamente o inserendo codice.
-   I driver del kernel possono hackerare la memoria del processo multimediale.
-   Il contenuto potrebbe essere inviato all'esterno del sistema su un supporto non protetto. La protezione dei collegamenti è progettata per attenuare questa minaccia.

## <a name="design-of-the-protected-environment"></a>Progettazione dell'ambiente protetto

Un ambiente protetto viene eseguito in un processo protetto separato dall'applicazione multimediale. La funzionalità processo protetto di Windows Vista impedisce ad altri processi di accedere al processo protetto.

Quando viene creato un processo protetto, i componenti principali del kernel identificano i componenti e i plug-in non attendibili, in modo che l'ambiente protetto possa rifiutarne il caricamento. Un componente attendibile è uno firmato correttamente da Microsoft. Il kernel tiene traccia anche dei moduli che li caricano, consentendo all'ambiente protetto di arrestare la riproduzione del contenuto protetto se viene caricato un modulo non attendibile. Prima del caricamento di un componente kernel, il kernel verifica se è attendibile. In caso contrario, i componenti attendibili già presenti nel file PE rifiutano di elaborare contenuto protetto. Per abilitare questa operazione, i componenti PE eseguono periodicamente un handshake protetto da crittografia con il kernel. Se è presente un componente della modalità kernel non attendibile, l'handshake ha esito negativo e indica al PE che un componente non attendibile esiste.

Se un componente attendibile viene compromesso, dopo la scadenza del processo può essere revocato. Microsoft fornisce un meccanismo di rinnovo per installare una versione più recente attendibile, se disponibile.

## <a name="protected-media-path"></a>Percorso supporto protetto

Il percorso multimediale protetto (PMP) è il file eseguibile PE primario per Media Foundation. Il PMP è estensibile, in modo che possano essere supportati i meccanismi di protezione del contenuto di terze parti.

Il PMP accetta il contenuto protetto e i criteri associati da qualsiasi origine Media Foundation usando qualsiasi sistema di protezione del contenuto, inclusi quelli forniti da terze parti. Invia il contenuto a qualsiasi sink di Media Foundation, purché il sink sia conforme ai criteri specificati dall'origine. Supporta inoltre le trasformazioni tra l'origine e il sink, incluse le trasformazioni di terze parti, purché siano attendibili.

Il PMP viene eseguito in un processo protetto isolato dall'applicazione multimediale. L'applicazione è in grado di scambiare i messaggi di comando e controllo con il PMP, ma non ha accesso al contenuto dopo che è stato passato a PMP. La figura seguente illustra questo processo.

![diagramma del percorso multimediale protetto](images/pmp04.png)

Le caselle ombreggiate rappresentano i componenti che possono essere forniti da terze parti. Tutti i componenti creati nel processo protetto devono essere firmati e attendibili.

L'applicazione crea un'istanza della sessione multimediale all'interno del processo protetto e riceve un puntatore a una sessione multimediale proxy, che effettua il marshalling dei puntatori di interfaccia attraverso il limite del processo.

L'origine multimediale può essere creata all'interno del processo dell'applicazione, come illustrato di seguito, o all'interno del processo protetto. Se l'origine multimediale viene creata all'interno del processo dell'applicazione, l'origine crea un proxy per se stesso nel processo protetto.

Tutti gli altri componenti della pipeline, ad esempio i decodificatori e i sink multimediali, vengono creati nel processo protetto. Se questi oggetti espongono interfacce personalizzate per le applicazioni, devono fornire un proxy/stub DCOM per effettuare il marshalling dell'interfaccia.

Per applicare i criteri ai contenuti protetti mentre passano attraverso la pipeline, PMP usa tre tipi di componenti: autorità di attendibilità di input (ITAs), autorità di attendibilità di output (OTA) e oggetti criteri. Questi componenti interagiscono per concedere o limitare i diritti di utilizzo del contenuto e per specificare le protezioni dei collegamenti che devono essere utilizzate per la riproduzione di contenuto, ad esempio High-bandwidth Digital protezione del contenuto (HDCP).

### <a name="input-trust-authorities"></a>Autorità di attendibilità di input

Un ITA viene creato da un'origine multimediale attendibile ed esegue diverse funzioni:

-   Specifica i diritti per l'utilizzo del contenuto. I diritti possono includere il diritto di riprodurre il contenuto, trasferirlo a un dispositivo e così via. Definisce un elenco ordinato di sistemi di protezione dell'output approvati e i criteri di output corrispondenti per ogni sistema. In ITA le informazioni vengono archiviate in un oggetto criteri.
-   Fornisce il decrittografia necessario per decrittografare il contenuto.
-   Stabilisce una relazione di trust con il modulo kernel nell'ambiente protetto per assicurarsi che ITA sia in esecuzione all'interno di un ambiente attendibile.

Un ITA è associato a un singolo flusso contenente contenuto protetto. Un flusso può avere un solo ITA e un'istanza di ITA può essere associata a un solo flusso.

### <a name="output-trust-authorities"></a>Autorità di attendibilità di output

Un OTA è associato a un output attendibile. OTA espone un'azione che l'output attendibile può eseguire sul contenuto, ad esempio la riproduzione o la copia. Il suo ruolo consiste nell'applicare uno o più sistemi di protezione dell'output necessari per ITA. OTA esegue una query sull'oggetto criteri fornito da ITA per determinare il sistema di protezione che deve applicare.

### <a name="policy-objects"></a>Oggetti Criteri

Un oggetto Criteri incapsula i requisiti di protezione del contenuto di un ITA. Viene usato dal motore dei criteri per negoziare il supporto della protezione del contenuto con un OTA. OTA oggetti Criteri di query per determinare i sistemi di protezione che devono applicare a ogni output del contenuto corrente.

### <a name="creating-objects-in-the-pmp"></a>Creazione di oggetti in PMP

Per creare un oggetto nel percorso multimediale protetto (PMP), [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) chiama [**IMFPMPHostApp:: ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid), con il formato **IStream** di input specificato nel modo seguente:

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>Panoramica della negoziazione dei criteri

Esistono tre requisiti fondamentali che devono essere soddisfatti prima che il contenuto protetto possa essere elaborato in PMP. Per prima cosa, il contenuto protetto deve essere inviato solo a output attendibili. In secondo luogo, è necessario applicare solo le azioni consentite a un flusso. Terzo, per riprodurre un flusso è necessario usare solo i sistemi di protezione dell'output approvati. Il motore dei criteri coordina tra ITAs e OTA per assicurarsi che questi requisiti siano soddisfatti.

Il modo più semplice per comprendere il processo consiste nell'esaminare un esempio semplificato che identifichi i passaggi necessari per riprodurre il contenuto di Advanced System Format (ASF) protetto da Windows Media Digital Rights Management (WMDRM).

Quando un utente avvia un'applicazione Player e apre un file ASF con un flusso audio protetto e un flusso video protetto, è necessario eseguire i passaggi seguenti:

1.  L'applicazione crea l'origine del supporto ASF e la sessione del percorso multimediale protetto (PMP). Media Foundation crea un processo PMP.
2.  L'applicazione crea una topologia parziale che contiene un nodo di origine audio connesso al renderer audio e un nodo di origine video connesso al renderer video avanzato (EVR). Per i renderer, l'applicazione non crea direttamente il renderer. Al contrario, l'applicazione crea nel processo non protetto un oggetto noto come oggetto di *attivazione*. Il PMP usa l'oggetto Activation per creare i renderer nel processo protetto. Per ulteriori informazioni sugli oggetti attivazione, vedere [oggetti attivazione](activation-objects.md).
3.  L'applicazione imposta la topologia parziale nella sessione PMP.
4.  La sessione PMP serializza la topologia e la passa all'host PMP nel processo protetto. L'host PMP Invia la topologia al motore dei criteri.
5.  Il caricatore della topologia chiama [**IMFInputTrustAuthority:: Decryptor**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) in ITAs e inserisce i decrittografatori nella topologia immediatamente a valle dei nodi di origine corrispondenti.
6.  Il caricatore della topologia inserisce i decodificatori audio e video a valle dei nodi Decrypter.
7.  Il motore dei criteri analizza i nodi inseriti per determinare se implementare l'interfaccia [**IMFTrustedOutput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) . I EVR e il renderer audio implementano entrambi **IMFTrustedOutput**, perché inviano dati all'esterno di PMP.
8.  Ogni ITA conferma che l'esecuzione avviene all'interno di un processo protetto mediante l'esecuzione di un handshake crittografico con un modulo kernel dell'ambiente protetto.
9.  Per ogni flusso, il motore dei criteri negozia i criteri ottenendo un oggetto criteri da ITA e passandolo a OTA. OTA fornisce un elenco dei sistemi di protezione supportati e l'oggetto criterio indica quali sistemi di protezione devono essere applicati, insieme alle impostazioni corrette. Il OTA applica quindi queste impostazioni. In caso contrario, il contenuto viene bloccato.

## <a name="revocation-and-renewal"></a>Revoca e rinnovo

Un componente attendibile può essere revocato se viene compromesso o viene individuato per violare i contratti di licenza in cui è stato inizialmente considerato attendibile. Un meccanismo di rinnovo esiste per installare una versione più recente e più attendibile del componente.

I componenti attendibili vengono firmati utilizzando un certificato crittografico. Microsoft pubblica un elenco di revoche globali (GRL) che identifica i componenti che sono stati revocati. GRL è firmato digitalmente per garantirne l'autenticità. I proprietari del contenuto possono garantire, tramite il meccanismo dei criteri, che la versione corrente di GRL sia presente nel computer dell'utente.

## <a name="output-link-protection"></a>Protezione del collegamento di output

Quando viene visualizzato il contenuto video Premium, i frame decrittografati e non compressi passano attraverso un connettore fisico al dispositivo di visualizzazione. I provider di contenuti possono richiedere che i fotogrammi video siano protetti a questo punto, mentre si spostano sul connettore fisico. A questo scopo esistono diversi meccanismi di protezione, tra cui High-Bandwidth Digital protezione del contenuto (HDCP) e DisplayPort protezione del contenuto (DPCP). Il video OTA impone queste protezioni usando l' [Output Protection Manager](output-protection-manager.md) (OPM). L'output Protection Manager invia comandi al driver di grafica e il driver di grafica impone tutti i meccanismi di protezione dei collegamenti richiesti dai criteri.

![diagramma che mostra la relazione tra il video OTA e OPM.](images/pmp05.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[protezione del contenuto basate su GPU](gpu-based-content-protection.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> <dt>

[Sessione multimediale PMP](pmp-media-session.md)
</dt> </dl>

 

 

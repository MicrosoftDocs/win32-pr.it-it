---
description: 'Questo argomento illustra tre argomenti correlati: ambiente protetto, gateway di interoperabilità dei supporti e revoca e rinnovo.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Percorso del supporto protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ebb2b22e6ad887134f91e93b43a698afdef0ebc36e1521d70e5e17fefedd8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035029"
---
# <a name="protected-media-path"></a>Percorso del supporto protetto

Questo argomento illustra tre argomenti correlati: ambiente protetto, gateway di interoperabilità dei supporti e revoca e rinnovo.

-   Un ambiente protetto (PE) è un set di tecnologie che consente al contenuto protetto di fluire da e attraverso Windows Vista in modo protetto. Tutti i componenti all'interno di un ambiente protetto sono attendibili e il processo è protetto da manomissioni.
-   Il percorso del supporto protetto (PMP) è un eseguibile eseguito in un ambiente protetto.
-   Se un componente attendibile nel pe viene compromesso, al termine del processo verrà revocato. Tuttavia, Microsoft offre un meccanismo di rinnovo per installare una versione attendibile più recente del componente quando ne diventa disponibile una.

Per informazioni sulla firma del codice dei componenti multimediali protetti, vedere l'white paper code [signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).

In questo argomento sono incluse le sezioni seguenti:

-   [Ambiente protetto](#protected-environment)
-   [Progettazione dell'ambiente protetto](#design-of-the-protected-environment)
-   [Percorso del supporto protetto](#protected-media-path)
    -   [Autorità di attendibilità di input](#input-trust-authorities)
    -   [Autorità di attendibilità di output](#output-trust-authorities)
    -   [Oggetti criteri](#policy-objects)
    -   [Creazione di oggetti in PMP](#creating-objects-in-the-pmp)
-   [Panoramica della negoziazione dei criteri](#overview-of-policy-negotiation)
-   [Revoca e rinnovo](#revocation-and-renewal)
-   [Protezione del collegamento di output](#output-link-protection)
-   [Argomenti correlati](#related-topics)

## <a name="protected-environment"></a>Ambiente protetto

La protezione del contenuto include più tecnologie, ognuna delle quali tenta di garantire che il contenuto non possa essere usato in modo incoerente con la finalità del proprietario o del provider di contenuti. Queste tecnologie includono la protezione della copia, la protezione dei collegamenti, l'accesso condizionale e digital rights management (DRM). La base di ogni elemento è l'attendibilità: l'accesso al contenuto viene concesso solo ai componenti software che rispettano le condizioni per l'utilizzo assegnate a tale contenuto.

Per ridurre al minimo le minacce contro il contenuto protetto, Windows Vista e Media Foundation Software consentono l'esecuzione di codice attendibile in un ambiente protetto. Un pe è un set di componenti, linee guida e strumenti progettati per aumentare la protezione dalla pirateria dei contenuti.

Prima di esaminare più da vicino il pe, è importante comprendere le minacce progettate per ridurre al minimo le minacce. Si supponga di eseguire un'applicazione multimediale in un processo in modalità utente. L'applicazione è collegata alle varie LIBRERIE (Dynamic Link Libraries) che contengono plug-in multimediali, ad esempio decodificatori. Anche altri processi vengono eseguiti in modalità utente e nel kernel vengono caricati vari driver. Se non è presente alcun meccanismo di attendibilità, esistono le minacce seguenti:

-   L'applicazione può accedere direttamente ai supporti protetti o violare la memoria del processo.
-   I plug-in possono accedere direttamente al contenuto o violare la memoria del processo.
-   Altri processi possono violare la memoria del processo multimediale direttamente o tramite l'inserimento di codice.
-   I driver del kernel possono violare la memoria del processo multimediale.
-   Il contenuto potrebbe essere inviato all'esterno del sistema tramite un supporto non protetto. La protezione dei collegamenti è progettata per attenuare questa minaccia.

## <a name="design-of-the-protected-environment"></a>Progettazione dell'ambiente protetto

Un ambiente protetto viene eseguito in un processo protetto separato dall'applicazione multimediale. La funzionalità di processo protetto di Windows Vista impedisce ad altri processi di accedere al processo protetto.

Quando viene creato un processo protetto, i componenti principali del kernel identificano componenti e plug-in non attendibili in modo che l'ambiente protetto possa rifiutare di caricarli. Un componente attendibile è un componente firmato in modo appropriato da Microsoft. Il kernel tiene inoltre traccia dei moduli caricati al suo interno, consentendo all'ambiente protetto di arrestare la riproduzione di contenuto protetto se viene caricato un modulo non attendibile. Prima di caricare un componente del kernel, il kernel verifica se è attendibile. In caso contrario, i componenti attendibili già presenti nel file PE rifiutano di elaborare il contenuto protetto. A tale scopo, i componenti PE eseguono periodicamente un handshake protetto da crittografia con il kernel. Se è presente un componente in modalità kernel non attendibile, l'handshake ha esito negativo e indica al pe che esiste un componente non attendibile.

Se un componente attendibile viene compromesso, al termine del processo può essere revocato. Microsoft offre un meccanismo di rinnovo per installare una versione attendibile più recente, se disponibile.

## <a name="protected-media-path"></a>Percorso del supporto protetto

Il percorso del supporto protetto (PMP) è l'eseguibile PE primario per Media Foundation. Il PMP è estendibile, quindi è possibile che siano supportati meccanismi di protezione del contenuto di terze parti.

Il PMP accetta contenuti protetti e criteri associati da qualsiasi origine Media Foundation usando qualsiasi sistema di protezione del contenuto, inclusi quelli forniti da terze parti. Invia il contenuto a Media Foundation sink, purché il sink sia conforme ai criteri specificati dall'origine. Supporta anche le trasformazioni tra l'origine e il sink, incluse le trasformazioni di terze parti, purché siano attendibili.

Il file PMP viene eseguito in un processo protetto isolato dall'applicazione multimediale. L'applicazione ha solo la possibilità di scambiare messaggi di comando e di controllo con il PMP, ma non ha accesso al contenuto dopo che è stato passato al PMP. La figura seguente illustra questo processo.

![Diagramma del percorso del supporto protetto](images/pmp04.png)

Le caselle ombreggiate rappresentano i componenti che potrebbero essere forniti da terze parti. Tutti i componenti creati all'interno del processo protetto devono essere firmati e considerati attendibili.

L'applicazione crea un'istanza della sessione multimediale all'interno del processo protetto e riceve un puntatore a una sessione multimediale proxy, che effettua il marshalling dei puntatori a interfaccia attraverso il limite del processo.

L'origine multimediale può essere creata all'interno del processo dell'applicazione, come illustrato di seguito, o all'interno del processo protetto. Se l'origine multimediale viene creata all'interno del processo dell'applicazione, l'origine crea un proxy per se stesso nel processo protetto.

Tutti gli altri componenti della pipeline, ad esempio decodificatori e sink multimediali, vengono creati nel processo protetto. Se questi oggetti espongono interfacce personalizzate per le applicazioni, devono fornire un proxy/stub DCOM per effettuare il marshalling dell'interfaccia.

Per applicare i criteri al contenuto protetto durante il flusso attraverso la pipeline, il PMP usa tre tipi di componenti: autorità di attendibilità di input (ITA), autorità di attendibilità di output (OTA) e oggetti criteri. Questi componenti funzionano insieme per concedere o limitare i diritti per l'uso del contenuto e per specificare le protezioni dei collegamenti che devono essere usate durante la riproduzione del contenuto, ad esempio High-bandwidth Digital Content Protection (HDCP).

### <a name="input-trust-authorities"></a>Autorità di attendibilità di input

Un ita viene creato da un'origine di supporti attendibile ed esegue diverse funzioni:

-   Specifica i diritti per l'uso del contenuto. I diritti possono includere il diritto di riprodurre il contenuto, trasferirlo in un dispositivo e così via. Definisce un elenco ordinato di sistemi di protezione dell'output approvati e i criteri di output corrispondenti per ogni sistema. L'ITA archivia queste informazioni in un oggetto criteri.
-   Fornisce il decrittografo necessario per decrittografare il contenuto.
-   Stabilisce una relazione di trust con il modulo kernel nell'ambiente protetto, per garantire che l'ita sia in esecuzione all'interno di un ambiente attendibile.

Un ita è associato a un singolo flusso contenente contenuto protetto. Un flusso può avere un solo ITA e un'istanza di ita può essere associata a un solo flusso.

### <a name="output-trust-authorities"></a>Autorità di attendibilità di output

Un OTA è associato a un output attendibile. L'OTA espone un'azione che l'output attendibile può eseguire sul contenuto, ad esempio la riproduzione o la copia. Il suo ruolo è quello di applicare uno o più sistemi di protezione dell'output richiesti dall'ITA. L'OTA esegue una query sull'oggetto criteri fornito da ITA per determinare il sistema di protezione da applicare.

### <a name="policy-objects"></a>Oggetti criteri

Un oggetto criteri incapsula i requisiti di protezione del contenuto di un ambiente ITA. Viene usato dal motore dei criteri per negoziare il supporto della protezione del contenuto con un OTA. Gli OTA eserciteranno query sugli oggetti criteri per determinare i sistemi di protezione che devono applicare a ogni output del contenuto corrente.

### <a name="creating-objects-in-the-pmp"></a>Creazione di oggetti in PMP

Per creare un oggetto nel percorso del supporto protetto (PMP), [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) chiama [**IMFPMPHostApp::ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid), con l'IStream di input specificato formattato nel modo seguente: 

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

Esistono tre requisiti fondamentali che devono essere soddisfatti prima che il contenuto protetto possa essere elaborato nel PMP. In primo luogo, il contenuto protetto deve essere inviato solo a output attendibili. In secondo piano, a un flusso devono essere applicate solo le azioni consentite. Terzo, solo i sistemi di protezione dell'output approvati devono essere usati per riprodurre un flusso. Il motore dei criteri si coordina tra ITA e OTA per garantire che questi requisiti siano soddisfatti.

Il modo più semplice per comprendere il processo è quello di illustrare un esempio semplificato che identifica i passaggi necessari per riprodurre contenuto ASF (Advanced System Format) protetto da Windows Media Digital Rights Management (WMDRM).

Quando un utente avvia un'applicazione lettore e apre un file ASF con un flusso audio protetto e un flusso video protetto, è necessario eseguire la procedura seguente:

1.  L'applicazione crea l'origine del supporto ASF e la sessione PMP (Protected Media Path). Media Foundation crea un processo PMP.
2.  L'applicazione crea una topologia parziale che contiene un nodo di origine audio connesso al renderer audio e un nodo di origine video connesso al renderer video avanzato (EVR). Per i renderer, l'applicazione non crea direttamente il renderer. Al contrario, l'applicazione crea nel processo non protetto un oggetto noto come oggetto *di attivazione*. PMP usa l'oggetto di attivazione per creare i renderer nel processo protetto. Per altre informazioni sugli oggetti di attivazione, vedere [Oggetti di attivazione.](activation-objects.md)
3.  L'applicazione imposta la topologia parziale nella sessione PMP.
4.  La sessione PMP serializza la topologia e la passa all'host PMP nel processo protetto. L'host PMP invia la topologia al motore dei criteri.
5.  Il caricatore della topologia chiama [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) negli ITA e inserisce i decrittografatori nella topologia immediatamente a valle dei nodi di origine corrispondenti.
6.  Il caricatore della topologia inserisce i decodificatori audio e video a valle dei nodi del decrypter.
7.  Il motore dei criteri analizza i nodi inseriti per determinare se un elemento implementa [**l'interfaccia IMFTrustedOutput.**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) L'EVR e il renderer audio implementano **entrambi IMFTrustedOutput**, perché inviano dati all'esterno del PMP.
8.  Ogni ITA conferma che è in esecuzione all'interno di un processo protetto eseguendo un handshake crittografico con un modulo kernel dell'ambiente protetto.
9.  Per ogni flusso, il motore dei criteri negozia i criteri ottenendo un oggetto criteri dall'ITA e passandolo all'OTA. L'OTA fornisce un elenco dei sistemi di protezione supportati e l'oggetto criteri indica quali sistemi di protezione devono essere applicati, insieme alle impostazioni corrette. L'OTA applica quindi queste impostazioni. Se non è possibile eseguire questa operazione, il contenuto viene bloccato.

## <a name="revocation-and-renewal"></a>Revoca e rinnovo

Un componente attendibile può essere revocato se viene compromesso o viene rilevato che viola i contratti di licenza in base ai quali è stato inizialmente considerato attendibile. Esiste un meccanismo di rinnovo per installare una versione più recente e attendibile del componente.

I componenti attendibili vengono firmati usando un certificato crittografico. Microsoft pubblica un elenco di revoche globale che identifica i componenti revocati. La firma GRL è firmata digitalmente per garantirne l'autenticità. I proprietari di contenuto possono garantire, tramite il meccanismo dei criteri, che la versione corrente della grl sia presente nel computer dell'utente.

## <a name="output-link-protection"></a>Protezione del collegamento di output

Quando viene visualizzato il contenuto video Premium, i fotogrammi decrittografati e non compressi attraversano un connettore fisico fino al dispositivo di visualizzazione. I provider di contenuti possono richiedere che i fotogrammi video siano protetti a questo punto, mentre attraversano il connettore fisico. A questo scopo esistono vari meccanismi di protezione, tra cui High-Bandwidth Digital protezione del contenuto (HDCP) e DisplayPort protezione del contenuto (DPCP). Il video OTA applica queste protezioni usando [Output Protection Manager](output-protection-manager.md) (OPM). Output Protection Manager invia comandi al driver di grafica e il driver di grafica applica tutti i meccanismi di protezione dei collegamenti richiesti dai criteri.

![diagramma che mostra la relazione tra il video ota e opm.](images/pmp05.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Impostazioni basate su GPU protezione del contenuto](gpu-based-content-protection.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> <dt>

[Sessione di supporti PMP](pmp-media-session.md)
</dt> </dl>

 

 

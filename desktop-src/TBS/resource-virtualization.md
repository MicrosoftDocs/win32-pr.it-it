---
title: Virtualizzazione delle risorse
description: Virtualizzazione delle risorse
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711818"
---
# <a name="resource-virtualization"></a>Virtualizzazione delle risorse

La funzione principale di TBS consiste nel condividere in modo efficiente alcune risorse TPM limitate: chiavi, autorizzazioni e sessioni di trasporto.

Quando viene creata un'istanza di una di queste risorse, TBS crea un'istanza virtuale della risorsa e restituisce un handle a questa istanza virtuale nel flusso del comando risultante, anziché nell'istanza dell'handle effettiva restituita dal TPM. TBS mantiene internamente un mapping tra l'handle virtuale e l'handle effettivo. Se il TPM esaurisce lo spazio per conservare più risorse di un determinato tipo, le istanze esistenti della risorsa vengono salvate e eliminate in modo selettivo finché il TPM non è in grado di mantenere la nuova risorsa. Quando le risorse precedenti sono nuovamente obbligatorie, TBS carica i contesti salvati (salvando e rimuovendo altre risorse se necessario) prima di inviare il comando.

Tutta la virtualizzazione in TBS viene eseguita per conto di un contesto specifico. Ogni contesto può accedere solo alle risorse virtuali create in modo specifico per suo conto, nonché alle risorse fisiche sul TPM che corrispondono a tali risorse virtuali. Per impostazione predefinita, il numero totale di tutte le risorse virtualizzate è limitato a 500. Questo numero può essere modificato creando o modificando un valore **DWORD** del registro di sistema denominato **MaxResources** in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**. È possibile osservare l'utilizzo delle risorse TBS in tempo reale usando lo strumento Performance Monitor per tenere traccia del numero di risorse TBS. Questa restrizione è diventata obsoleta con Windows 8 e Windows Server 2012.

Risorse TPM limitate non virtualizzate da TBS (ad esempio, contatori e archivio NV) devono essere condivise in modo cooperativo tra gli stack di software.

> [!Note]  
> Questa virtualizzazione dell'handle causa l'esito negativo dei comandi che includono handle di chiave nel calcolo di parametri di autorizzazione HMAC. Di conseguenza, molti comandi deprecati nella versione 1,2 del TPM non possono essere usati dal software applicativo nell'ambiente TBS.

 

## <a name="resource-limits"></a>Limiti delle risorse

Il TPM consente ai chiamanti di eseguire query sulle proprie funzionalità per determinare la quantità di spazio disponibile per determinati tipi di risorse. Alcuni di questi limiti di risorse, ad esempio la quantità di spazio disponibile per chiavi, sessioni di autorizzazione e sessioni di trasporto, vengono efficacemente estesi da TBS attraverso la virtualizzazione. Le limitazioni di TBS, che sono controllate dall'impostazione del registro di sistema **MaxResources** , sono in genere molto più grandi delle limitazioni effettive dell'hardware TPM sottostante. Non viene fornito alcun meccanismo per l'esecuzione di query sulle limitazioni di TBS separatamente rispetto ai limiti hardware del TPM. Questa limitazione di TBS è diventata obsoleta con Windows 8 e Windows Server 2012.

## <a name="keys"></a>Chiavi

TBS virtualizza gli handle chiave in modo che le chiavi possano essere scaricate in modo trasparente dal TPM quando non vengono usate e ricaricate nel TPM quando sono necessarie. Quando viene creato un tasto, TBS associa un handle virtuale alla chiave caricata. Lo stesso handle virtuale viene usato per la durata della risorsa. Gli handle di chiave virtuale sono validi solo nel contesto che li ha creati e le risorse associate non vengono mantenute oltre la durata del contesto.

-   Creazione di chiavi con TPM \_ LoadKey2

    Se viene creata una chiave usando il comando TPM \_ LoadKey2, TPM2 \_ CREATEPRIMARY, TPM2 \_ Load o TPM2 \_ LoadExternal, TBS sostituisce l'handle nel flusso di byte restituito con un handle di chiave virtuale di sua scelta. Di conseguenza, TBS garantisce che ogni handle virtuale sia univoco. Se TBS rileva un conflitto (un evento estremamente improbabile), TBS Scarica la chiave dal TPM e informa il software chiamante. Il software può quindi inviare nuovamente l'operazione. Questo processo può essere ripetuto fino a quando TBS non ottiene un handle di chiave univoco.

-   Cancellazione di chiavi

    TBS invalida l'handle di chiave virtuale quando riceve un \_ messaggio TPM FlushSpecific o TPM2 \_ FlushContext per tale handle virtuale dal contesto client. Se la chiave è fisicamente presente nel TPM quando viene ricevuto il messaggio di scaricamento, TBS Scarica la chiave dal TPM in quel momento.

-   Rimozione temporanea di chiavi

    Quando si rimuove una chiave dal TPM per creare spazio per un nuovo elemento, TBS esegue un \_ comando TPM SaveContext o TPM2 \_ ContextSave sulla chiave prima di rimuoverlo.

-   Ripristino di chiavi

    Quando un comando che fa riferimento a una chiave caricata viene inviato a TBS, garantisce che la chiave sia fisicamente presente nel TPM. Se la chiave non è presente, TBS lo ripristina con una chiamata a TPM \_ LoadContext o TPM2 \_ ContextLoad. Se una chiave non può essere ripristinata nel TPM, TBS restituisce un HANDLE di chiave TPM \_ E \_ non valido \_ come risultato del TPM.

TBS sostituisce ogni handle virtuale associato a una chiave in un flusso di comandi con l'handle fisico della chiave caricata nel TPM. Se un comando viene inviato con un handle virtuale non riconosciuto da TBS nel contesto del chiamante, TBS formatta un flusso di errore per il chiamante con un HANDLE di tasti TPM \_ E non \_ valido \_ .

## <a name="authorization-sessions"></a>Sessioni di autorizzazione

Le sessioni di autorizzazione vengono create chiamando TPM \_ OIAP, TPM \_ OSAP o TPM \_ DSAP. In ogni caso, il flusso di byte restituito contiene l'handle del TPM fisico della sessione di autorizzazione appena creata. TBS sostituisce questo oggetto con un handle virtuale. Quando viene successivamente fatto riferimento alla sessione di autorizzazione, TBS sostituisce l'handle virtuale nel flusso di comandi con l'handle fisico della sessione di autorizzazione. TBS garantisce che la durata della sessione di autorizzazione virtuale corrisponda a quella della sessione di autorizzazione fisica. Se un client tenta di usare un handle virtuale scaduto, TBS formatta un flusso di errore con errore \_ INVALIDAUTHHANDLE TPM.

Gli slot di sessione sono limitati e la TBS può esaurire gli slot esterni in cui salvare i contesti di sessione di autorizzazione. In tal caso, TBS sceglie una sessione di autorizzazione da invalidare in modo che il nuovo contesto possa essere salvato correttamente. Un'applicazione che tenta di utilizzare il contesto precedente dovrà creare nuovamente la sessione di autorizzazione.

TBS invalida la sessione di autorizzazione virtuale quando si verifica uno dei casi seguenti:

-   Il flag di utilizzo continuo associato alla sessione di autorizzazione nel flusso di comandi restituito dal TPM è **false**.
-   Un comando che usa una sessione di autorizzazione ha esito negativo.
-   Viene eseguito un comando che invalida la sessione di autorizzazione associata al comando (ad esempio TPM \_ CreateWrapKey).
-   Una chiave associata a una sessione OSAP o DSAP viene eliminata dal TPM con una chiamata a TPM \_ FlushSpecific o TPM2 \_ FlushContext (indipendentemente dal fatto che il comando sia stato originato da TBS o con software di livello superiore).

    TBS Risincronizza automaticamente le sessioni di autorizzazione dopo l'esecuzione corretta di determinati comandi non deterministici per assicurarsi che lo stato di TBS rimanga coerente con lo stato TPM. I comandi interessati sono:

    -   \_Gestione del \_ delegato di \_ gestione del TPM
    -   \_ \_ CreateOwnerDelegation delegato dell'ORD TPM \_
    -   \_ \_ LoadOwnerDelegation delegato dell'ORD TPM \_

In ognuno dei casi seguenti la sessione di autorizzazione nel TPM viene scaricata automaticamente dal TPM:

-   Creazione di sessioni di autorizzazione

    Gli handle della sessione di autorizzazione virtuale sono validi solo nel contesto che li ha creati e le risorse associate non vengono mantenute oltre la durata del contesto associato.

-   Cancellazione delle sessioni di autorizzazione

    TBS invalida la sessione di autorizzazione virtuale se riceve un \_ comando TPM FlushSpecific o TPM2 \_ FlushContext per l'handle virtuale dal contesto client. Se la sessione di autorizzazione è fisicamente presente nel TPM quando viene ricevuto il comando di scaricamento, TBS Scarica immediatamente la sessione fisica dal TPM.

-   Rimozione temporanea di sessioni di autorizzazione

    Quando si rimuove una sessione di autorizzazione dal TPM per creare spazio per una nuova entità, TBS esegue TPM \_ SaveContext o TPM2 \_ ContextSave in tale sessione di autorizzazione.

-   Ripristino di sessioni di autorizzazione

    Quando un comando TPM autorizzato viene inviato a TBS, la TBS garantisce che tutte le sessioni di autorizzazione virtuali a cui viene fatto riferimento nel comando siano fisicamente presenti sul TPM. Se una delle sessioni di autorizzazione non è presente, TBS le ripristina con una chiamata a TPM \_ LoadContext o TPM2 \_ ContextLoad. Se una sessione di autorizzazione non può essere ripristinata nel TPM, TBS restituisce \_ un \_ handle non valido TPM e \_ come risultato del TPM.

TBS sostituisce ogni handle virtuale associato a una sessione di autorizzazione in un flusso di comandi con l'handle fisico della sessione di autorizzazione caricata nel TPM.

Se un comando viene inviato con un handle virtuale non riconosciuto da TBS nel contesto del chiamante, TBS formatta un flusso di errore per il chiamante con l'handle di errore TPM \_ E non \_ valido \_ .

## <a name="transport-sessions"></a>Sessioni di trasporto

> [!Note]  
> La gestione delle sessioni di trasporto, come descritto di seguito, è specifica di Windows Vista e Windows Server 2008.

 

Le sessioni di trasporto sono un meccanismo fornito dal TPM che consente a uno stack software di crittografare i dati in un comando mentre passano tra il software e il TPM. In questo modo si impedisce a un antagonista di intercettare i dati mentre passano sul bus hardware.

> [!IMPORTANT]
> Vengono crittografati solo i dati del payload. I comandi eseguiti possono comunque essere identificati.

 

Sfortunatamente, questo meccanismo impedisce anche a TBS di esaminare i dati del payload. Nella maggior parte dei casi non si tratta di un problema perché TBS modifica solo gli handle, non i dati del payload. Tuttavia, nel caso di LoadContext TPM \_ , l'handle di risorsa restituito viene coperto dalla crittografia. Pertanto, TBS impedisce ai tentativi di eseguire un' \_ operazione LOADCONTEXT TPM coperta da una sessione di trasporto.

TBS blocca i comandi seguenti nella sessione di trasporto:

-   \_ESTABLISHTRANSPORT TPM
-   \_EXECUTETRANSPORT TPM
-   \_Handle di terminazione TPM \_
-   \_LOADKEY TPM
-   \_EVICTKEY TPM
-   \_SAVEKEYCONTEXT TPM
-   \_LOADKEYCONTEXT TPM
-   \_SAVEAUTHCONTEXT TPM
-   \_LOADAUTHCONTEXT TPM
-   \_SAVECONTEXT TPM
-   \_LOADCONTEXT TPM
-   \_FLUSHSPECIFIC TPM

Quando uno di questi comandi è coperto da una sessione di trasporto, TBS restituisce il \_ comando TPM E \_ Embedded non \_ \_ supportato come risultato del TPM.

Gli handle di sessione di trasporto vengono virtualizzati in modo analogo agli handle di chiave e agli handle di autorizzazione. Nel TPM è disponibile un numero limitato di slot del contesto di sessione di trasporto salvati.

TBS invalida la sessione di trasporto virtuale se si verifica uno dei casi seguenti:

-   Il flag di utilizzo continuo associato alla sessione di trasporto nel flusso del comando restituito dal TPM è **false**.

    Come per le sessioni di autorizzazione precedenti, TBS Risincronizza automaticamente le sessioni di trasporto dopo l'esecuzione corretta di determinati comandi non deterministici per garantire che lo stato di TBS rimanga coerente con lo stato del TPM. I comandi interessati sono:

    -   \_Gestione del \_ delegato di \_ gestione del TPM
    -   \_ \_ CreateOwnerDelegation delegato dell'ORD TPM \_
    -   \_ \_ LoadOwnerDelegation delegato dell'ORD TPM \_

In ognuno di questi casi, la sessione di trasporto nel TPM verrà scaricata automaticamente dal TPM:

-   Creazione di sessioni di trasporto

    TBS crea un handle virtuale per ogni sessione di trasporto creata da un client. Gli handle di trasporto virtuali sono validi solo nel contesto che li ha creati e le risorse associate non vengono mantenute oltre la durata del contesto associato.

-   Cancellazione delle sessioni di trasporto

    TBS invalida la sessione di trasporto virtuale se riceve un \_ comando TPM FlushSpecific per l'handle virtuale dal contesto client. Se la sessione di trasporto è fisicamente presente nel TPM quando viene ricevuto il comando di scaricamento, TBS Scarica immediatamente la sessione fisica dal TPM.

-   Rimozione temporanea di sessioni di trasporto

    Quando si rimuove una sessione di trasporto dal TPM per creare spazio per una nuova entità, TBS esegue \_ SAVECONTEXT TPM in tale sessione di trasporto.

-   Ripristino di sessioni di trasporto

    Quando un \_ comando TPM ExecuteTransport viene inviato a TBS, TBS garantisce che la sessione di trasporto a cui viene fatto riferimento nel comando sia fisicamente presente sul TPM. Se la sessione di trasporto non è presente, TBS lo ripristina con una chiamata a TPM \_ LoadContext.

TBS sostituisce l'handle virtuale associato alla sessione di trasporto in un flusso di comandi con l'handle fisico della sessione di trasporto caricata nel TPM. Se un comando viene inviato con un handle virtuale non riconosciuto da TBS nel contesto del chiamante, TBS formatta un flusso di errore per il chiamante utilizzando un \_ handle TPM E non \_ valido \_ .

## <a name="exclusive-transport-sessions"></a>Sessioni di trasporto esclusive

Le sessioni di trasporto con wrapper esclusivo consentono al software di primo livello di determinare se un altro software ha eseguito l'accesso al TPM durante una catena di comandi. Poiché non impediscono l'accesso al TPM da parte di altri software, forniscono solo al creatore della sessione di trasporto un metodo per determinare se si è verificato un altro accesso. TBS non esegue operazioni specifiche per ostacolare le sessioni di trasporto esclusive, ma è incompatibile. TBS tenta di duplicare il comportamento naturale del TPM grazie alla trasparenza, quindi non predilige i comandi dei contesti che stabiliscono una sessione di trasporto esclusiva. Se, ad esempio, il client B invia un comando quando il client A si trova in una sessione di trasporto esclusiva, invalida la sessione di trasporto esclusiva del client A.

I comandi avviati da TBS possono anche terminare la sessione di trasporto esclusivo. Questo errore si verifica quando il client A si trova in una sessione di trasporto esclusiva e un comando eseguito dal client A chiama una risorsa che non è fisicamente presente nel TPM. Questa situazione attiva il gestore della virtualizzazione di TBS per eseguire un \_ comando TPM LoadContext per fornire tale risorsa, che termina la sessione di trasporto esclusiva del client a.

 

 





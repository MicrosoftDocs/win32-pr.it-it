---
description: Il concetto di indirizzo è fondamentale per la maggior parte delle operazioni di comunicazione.
ms.assetid: 32fbd06b-f6f2-4024-b8d5-3d6eef16bca2
title: Indirizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6ad8f03b725a58d564c63f4c5c0d0165eed99a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314643"
---
# <a name="address"></a>Indirizzo

Il concetto di indirizzo è fondamentale per la maggior parte delle operazioni di comunicazione. Un indirizzo rappresenta una posizione in una rete. L'assegnazione locale di un indirizzo a una riga o a un canale si verifica in genere durante l'installazione del provider di servizi, ma può essere modificata in un secondo momento. Per informazioni dettagliate sulle procedure necessarie, vedere il Resource Kit del sistema operativo per i provider di servizi forniti da Microsoft e nella documentazione relativa al provider di servizi per prodotti non Microsoft.

Un singolo indirizzo può essere condiviso da più di un dispositivo di linea. Diversi fornitori di commuteri hanno nomi diversi per questo concetto, ad esempio il bridging degli indirizzi, il numero di directory con più aspetti (MADN) o l'aspetto con Bridge. Una chiamata in ingresso su un indirizzo condiviso viene offerta su tutte le righe associate all'indirizzo. Per una descrizione delle configurazioni riconosciute da TAPI, vedere [ \_ costanti LINEADDRESSSHARING](./lineaddresssharing--constants.md) .

L'indirizzo stesso è una stringa che identifica una posizione in una rete. Nel caso di una rete telefonica, l'indirizzo è un numero di telefono completo di codici nazionali o internazionali. Se la rete è basata su IP, l'indirizzo potrebbe essere un indirizzo IP. Vedere [ \_ costanti LINEADDRESSTYPE](lineaddresstype--constants.md) per i tipi di indirizzi definiti da TAPI. Un provider di servizi può definire tipi di indirizzi aggiuntivi.

## <a name="address-related-capabilities-and-messages"></a>Funzionalità e messaggi di Address-Related

Diversi indirizzi hanno caratteristiche, funzionalità e Stati diversi. I provider di servizi sono l'origine di tali informazioni. La funzionalità di query dispositivo e lo stato e i meccanismi di segnalazione degli eventi di TAPI forniscono a un'applicazione le informazioni per gestire gli indirizzi.

Le applicazioni acquisiscono queste informazioni elaborando gli eventi da TAPI o usando le operazioni di query. Questo consente a un'applicazione di prendere in considerazione i fattori, ad esempio se un indirizzo specificato supporta una funzionalità specifica, ad esempio [Park](park-ovr.md).

**TAPI 2. x:** Le applicazioni chiamano la funzione [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) per determinare le funzionalità di telefonia di ogni indirizzo e quindi ricevono queste informazioni in una struttura di dati [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) . In modo analogo, un'applicazione può chiamare [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) per un dispositivo a linee per determinare il numero di indirizzi assegnati alla riga, oltre ad altre informazioni.

**TAPI 3. x:** Le applicazioni utilizzano le [interfacce dell'oggetto Address](address-object-interfaces.md) per acquisire informazioni sulle funzionalità e sugli eventi degli indirizzi.

## <a name="storing-phone-numbers-in-electronic-address-books"></a>Archiviazione di numeri di telefono in rubriche elettroniche

Molti utenti scelgono di comporre le persone, le macchine fax, le bacheche e altre entità selezionando i relativi nomi da una rubrica. Il numero effettivo composto dipende dalla posizione geografica dell'utente e dalla modalità di connessione del dispositivo linea da usare. Ad esempio, un computer desktop può accedere a due righe, una connessa a un PBX, l'altra alla sede centrale della società telefonica. Quando si effettua una chiamata alla stessa entità, potrebbe essere necessario usare numeri diversi. (Per comporre il PBX, ad esempio, il computer potrebbe dover comporre un prefisso "9" per ottenere una riga esterna oppure è possibile che sia necessario un prefisso diverso per una chiamata eseguita tramite la sede centrale.) In alternativa, un utente può effettuare chiamate da un computer portatile e desidera utilizzare una singola rubrica statica anche quando viene chiamato da diverse posizioni o ambienti di telefonia. Le funzionalità di traduzione degli indirizzi di TAPI consentono all'utente di informare il computer della posizione corrente e il dispositivo di linea desiderato per la chiamata. TAPI gestisce quindi le eventuali differenze di composizione, senza richiedere alcuna modifica alla rubrica dell'utente. Un'applicazione usa la [conversione degli indirizzi](initiate-a-session-ovr.md) per convertire un indirizzo dal formato degli [indirizzi canonico](#canonical-addresses) al formato dell' [indirizzo di connessione](#dialable-addresses) .

Un argomento correlato è la gestione del monitoraggio delle chiamate in corso internazionale, ovvero il processo di ascolto di toni udibili, ad esempio il tono di composizione, i toni di informazioni speciali, i segnali di occupato e i toni di richiamata per determinare lo *stato* di una chiamata (avanzamento attraverso la rete). Poiché le cadenza e le frequenze dei toni di avanzamento delle chiamate variano a seconda del paese o dell'area geografica, il provider di servizi deve conoscere l'avanzamento della chiamata da seguire quando si effettua una chiamata in uscita internazionale. Pertanto, le applicazioni specificano il codice paese o regione di destinazione quando si posizionano le chiamate in uscita.

## <a name="canonical-addresses"></a>Indirizzi canonici

Il formato di indirizzo canonico è costituito da un numero di directory di universalmente costante. Per questo motivo, è consigliabile archiviare i numeri nelle rubriche con il formato canonico.

I dettagli seguenti riguardano ciò che viene considerato canonico per un indirizzo telefonico.

Un indirizzo telefonico canonico è una stringa di testo con la struttura seguente:

\+*CountryCode* Spazio \[ **(**_areacode_*_)_* spazio \] *SubscriberNumber* \| nome del *sottoindirizzo*  ^   CRLF...

I componenti di questa struttura sono descritti nella tabella seguente.



Componente

Significato

\+

Equivalente a Hex 2B. Indica che il numero che segue usa il formato canonico.

*CountryCode*

Stringa di dimensioni variabilmente contenente una o più cifre da "0" a "9" (esadecimale da 30 a 39, inclusi). Il *CountryCode* è delimitato dallo spazio seguente. Identifica il paese o l'area geografica in cui si trova l'indirizzo.

Space

Esattamente un carattere di spazio (hex 20). Viene usato per delimitare la fine della parte *CountryCode* di un indirizzo.

*AreaCode*

Stringa di dimensioni variabilmente che contiene zero o più cifre da "0" a "9" (esadecimale da 30 a 39, inclusi). *Areacode* è la parte relativa al codice di area dell'indirizzo ed è facoltativa. Se il codice di area è presente, deve essere preceduto da un solo carattere di parentesi aperta (28) ed essere seguito da un solo carattere di parentesi destra (29) e da un carattere di spazio (20).

*SubscriberNumber*

Stringa di dimensioni variabilmente contenente una o più cifre da "0" a "9" (esadecimale da 30 a 39, inclusi). Può includere anche altri caratteri di formattazione, inclusi i caratteri di controllo di composizione descritti nel formato di indirizzo di composizione:

 

Carattere

codifica esadecimale

 

! \#<br/> $<br/> \*<br/> ,<br/> ?<br/> @<br/> ABCD<br/> P<br/> T<br/> W<br/> abcd<br/> p<br/> u<br/> w<br/>

21 23<br/> 24<br/> 2A<br/> 2C<br/> 3F<br/> 40<br/> 41-44<br/> 50<br/> 54<br/> 77<br/> 61-64<br/> 70<br/> 74<br/> 79<br/>

 

Il numero del Sottoscrittore non deve contenere il carattere parentesi aperta o parentesi destra (che vengono usate solo per delimitare il prefisso), né contenere i caratteri " \| ", "^" o CRLF (che vengono usati per iniziare i campi seguenti). In genere, i caratteri non numerici nel numero del Sottoscrittore includono solo spazi, punti (".") e trattini ("-"). Tutti i caratteri non numerici consentiti visualizzati nel numero del Sottoscrittore vengono omessi dal *DialableString* restituito dalla funzione [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) , ma vengono conservati nel *DisplayableString*.

\|

Hex (7C). Se questo carattere facoltativo è presente, le informazioni che lo seguono fino alla successiva + \| ^ CRLF, o alla fine della stringa dell'indirizzo canonico, vengono considerate come informazioni sugli indirizzi subindirizzi, come per un sottoindirizzo ISDN.

*Sottoindirizzo*

Stringa di dimensioni variabilmente contenente un sottoindirizzo. La stringa è delimitata da + \| ^ CRLF o dalla fine della stringa dell'indirizzo. Durante la composizione, le informazioni relative ai subindirizzi vengono passate alla parte remota. Può trattarsi di un indirizzo ISDN o di un indirizzo di posta elettronica.

^

Hex (5E). Se questo carattere facoltativo è presente, le informazioni che lo seguono fino al CRLF successivo o alla fine della stringa dell'indirizzo canonico vengono considerate come un nome ISDN.

*Nome*

Stringa di dimensioni variabilmente trattata come informazioni sul nome. Il nome è delimitato da CRLF o dalla fine della stringa dell'indirizzo canonico e può contenere altri delimitatori. Durante la composizione, le informazioni sul nome vengono passate alla parte remota.

CRLF

Hex (0D) seguito da Hex (0A) ed è facoltativo. Se presente, indica che segue un altro numero canonico. Viene usato per separare più indirizzi canonici come parte di una singola stringa di indirizzo (multiplexing inverso). Ad esempio, la rappresentazione canonica del numero di telefono del centralino principale in Microsoft Corporation sarà:<br/> + 1 (425) 882-8080<br/>



 

## <a name="dialable-addresses"></a>Indirizzi di connessione remota

Il formato dell'indirizzo che è possibile comporre è il formato in cui un indirizzo viene passato a un provider di servizi che gestisce i numeri di telefono. Di seguito sono riportati i dettagli relativi agli indirizzi di connessione remota in una rete telefonica.

Il formato del numero che è possibile comporre consente la fornitura di più indirizzi di destinazione contemporaneamente. Questa possibilità può essere utile se il provider di servizi offre una forma di multiplexing inverso, impostando le chiamate a ognuna delle destinazioni specificate e quindi gestendo il flusso di informazioni come un singolo flusso multimediale a larghezza di banda elevata. L'applicazione percepisce questo gruppo di chiamate come una singola chiamata perché riceve solo un singolo handle di chiamata che rappresenta l'aggregazione delle singole chiamate telefoniche.

È anche possibile supportare il multiplexing inverso a livello di applicazione. A tale scopo, l'applicazione imposta una serie di chiamate singole e sincronizza i flussi multimediali.

Il *sottoindirizzo* è una funzionalità fornita su linee ISDN che consente di ottenere più informazioni rispetto a un singolo numero di telefono da usare per la composizione. Con queste informazioni aggiuntive è possibile specificare una singola estensione per telefoni, oppure, in un ambiente di elaborazione, un'applicazione specifica da avvisare. Altri parametri possono descrivere gli aspetti obbligatori di una connessione richiesta, ad esempio la frequenza e l'intervallo di tempo.

Se è supportato da un provider di servizi, l'applicazione include questo nell'indirizzo passato a qualsiasi operazione che ne richiede una.

Un indirizzo telefonico collegabile contiene informazioni sull'indirizzamento delle parti ed è parte della natura. Qualsiasi stringa di input che non inizia con un carattere "+" non deve essere in formato canonico e pertanto deve essere in formato di indirizzo configurabile e viene restituita all'applicazione non modificata. Un indirizzo che può essere composto da una stringa di testo con la struttura seguente:

*DialableNumber* \| *Sottoindirizzo*  ^  *Nome* CRLF...

I componenti di questa struttura sono forniti nella tabella seguente.



| Componente        | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DialableNumber* | Cifre e modificatori 0-9 A-D \* \# ,! W w P p T @ $? ; delimitato da \| ^ CRLF o dalla fine della stringa dell'indirizzo di connessione. Il segno più (+) è un carattere valido nelle stringhe di connessione. Indica che il numero di telefono è un numero internazionale completo. All'interno di *DialableNumber*, tenere presente le definizioni seguenti:<br/> 0-9 A-D \*\#<br/> Caratteri corrispondenti alle cifre DTMF e/o Pulse.<br/> |
| !                | Hex (21). Indica che nella stringa di connessione è necessario inserire un hookflash (uno-mezzo secondo OnHook, seguito da un Offhook di uno-metà secondo prima di continuare).                                                                                                                                                                                                                                                                                   |
| P p              | Hex (50) o Hex (70). Indica che la chiamata a impulsi deve essere utilizzata per le cifre che lo seguono.                                                                                                                                                                                                                                                                                                                                                |
| T t              | Hex (54) o Hex (74). Indica che la composizione del tono (DTMF) deve essere utilizzata per le cifre che lo seguono.                                                                                                                                                                                                                                                                                                                                          |
| ,                | Esadecimale (27). Indica che la composizione deve essere sospesa. La durata di una pausa è specifica del dispositivo e può essere recuperata dalle funzionalità del dispositivo della linea. Per fornire pause più lunghe, è possibile usare più virgole.                                                                                                                                                                                                                                 |
| W w              | Hex (57) o Hex (77). Una W maiuscola o minuscola indica che la composizione deve continuare solo dopo che è stato rilevato un tono di connessione.                                                                                                                                                                                                                                                                                                            |
| @                | Hex (40). Indica che la composizione è "Wait for quiet answer" prima di comporre il resto dell'indirizzo di connessione. Ciò significa attendere almeno una risponderia seguita da alcuni secondi di silenzio.                                                                                                                                                                                                                               |
| $                | Hex (24). Indica che per comporre le informazioni di fatturazione è necessario attendere un "segnale di fatturazione", ad esempio un tono di richiesta della carta di credito.                                                                                                                                                                                                                                                                                                              |
| ?                | Esadecimale (3F). Indica che l'utente deve essere richiesto prima di continuare con la composizione. Il provider non esegue effettivamente la richiesta, ma la presenza del "?" impone al provider di rifiutare la stringa come non valida, avvisando l'applicazione della necessità di suddividerla in parti e richiedere l'intervento dell'utente.                                                                                                                           |
| ;                | Hex (3B). Se posizionata alla fine di una stringa di indirizzo dialable parzialmente specificata, indica che le informazioni sul numero che è possibile comporre sono incomplete e in seguito verranno fornite ulteriori informazioni sugli indirizzi. Il componente ";" è consentito solo nella parte *DialableNumber* di un indirizzo.                                                                                                                                                       |
| \|               | Hex (7C) ed è facoltativo. Se presente, le informazioni che lo seguono fino al successivo + \| ^ CRLF o alla fine della stringa dell'indirizzo che si può comporre vengono considerate come informazioni sui subindirizzi, come per un sottoindirizzo ISDN.                                                                                                                                                                                                                                  |
| *Sottoindirizzo*     | Stringa di dimensioni variabilmente contenente un sottoindirizzo. La stringa è delimitata dal successivo + \| ^ CRLF o dalla fine della stringa dell'indirizzo. Quando si esegue la composizione, le informazioni relative ai subindirizzi vengono passate alla parte remota. Può trattarsi di un sottoindirizzo ISDN, un indirizzo di posta elettronica e così via.                                                                                                                                                                       |
| ^                | Hex (5E) ed è facoltativo. Se presente, le informazioni che lo seguono fino al CRLF successivo o alla fine della stringa di indirizzo che è possibile comporre vengono considerate come un nome ISDN.                                                                                                                                                                                                                                                                                |
| *Nome*           | Stringa di dimensioni variabilmente trattata come informazioni sul nome. Il nome è delimitato da CRLF o dalla fine della stringa dell'indirizzo di connessione. Quando si esegue la composizione, le informazioni sul nome vengono passate alla parte remota.                                                                                                                                                                                                                                                      |
| CRLF             | Hex (0D) seguito da Hex (0A). Se presente, questo carattere facoltativo indica che è presente un altro numero collegabile. Viene utilizzato per separare più indirizzi che è possibile comporre come parte di una singola stringa di indirizzo (per il multiplexing inverso).                                                                                                                                                                                           |



 

La conversione degli indirizzi può essere usata per tradurre un indirizzo dal formato canonico al formato di composizione.

 


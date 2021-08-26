---
description: È possibile usare le funzioni del Registro di sistema per raccogliere dati sulle prestazioni.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Uso delle funzioni del Registro di sistema per utilizzare i dati dei contatori
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 69f64f6e4cb44dd98d4f5097ca791054cd04c7e07219dc0e270cbfdff4cdbdc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033121"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Uso delle funzioni del Registro di sistema per utilizzare i dati dei contatori

Usare le funzioni [del Registro di](/windows/desktop/SysInfo/registry-functions) sistema per raccogliere dati sulle prestazioni dalla chiave speciale del Registro di `HKEY_PERFORMANCE_DATA` sistema.

I dati sulle prestazioni non vengono effettivamente archiviati nel Registro di sistema. Se si chiamano le funzioni del Registro di sistema, il sistema raccoglie i dati dal provider di dati delle prestazioni appropriato.

> [!Note]
> In genere non è consigliabile usare le funzioni del Registro di sistema per utilizzare i dati dei contatori. È invece [consigliabile usare le funzioni PDH (Performance Data Helper).](using-the-pdh-functions-to-consume-counter-data.md) Le funzioni PDH sono più facili da usare ed evitare molti problemi di prestazioni e affidabilità che possono verificarsi tramite un uso non corretto delle funzioni del Registro di sistema.

> [!Note]
> Non è possibile usare le funzioni del Registro di sistema se si scrivono Windows OneCore app. Usare invece le [funzioni consumer PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md).

Le funzioni del Registro di sistema sono l'API di basso livello per la raccolta di dati **dai provider V1.** Le funzioni del Registro di sistema supportano anche la raccolta di dati **dai provider V2** tramite un livello di traduzione che chiama nelle [funzioni consumer V2.](using-the-perflib-functions-to-consume-counter-data.md)

Per ottenere dati sulle prestazioni dal sistema locale, chiamare la [**funzione RegQueryValueEx.**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) Usare `HKEY_PERFORMANCE_DATA` come chiave. La prima chiamata apre la chiave. Non è necessario aprire prima la chiave in modo esplicito.

Per ottenere dati sulle prestazioni da un sistema remoto, chiamare la [**funzione RegConnectRegistry.**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) Usare il nome computer del sistema remoto e `HKEY_PERFORMANCE_DATA` usare come chiave. Questa chiamata recupera una chiave che rappresenta i dati sulle prestazioni per il sistema remoto. Usare questa chiave anziché `HKEY_PERFORMANCE_DATA` la chiave per recuperare i dati.

Assicurarsi di usare la [**funzione RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) per chiudere l'handle per la chiave al termine dell'ottenimento dei dati sulle prestazioni. Questo aspetto è importante sia per i casi locali che per i casi remoti:

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` non chiude effettivamente un handle del Registro di sistema, ma cancella tutti i dati memorizzati nella cache e libera le DLL delle prestazioni caricate.
- `RegCloseKey(hkeyRemotePerformanceData)` chiude l'handle nel Registro di sistema del computer remoto.

> [!IMPORTANT]
> Non chiamare durante `RegCloseKey(HKEY_PERFORMANCE_DATA)` `DLL_PROCESS_DETACH` .

Usare il `lpValueName` parametro della funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) per indicare le informazioni da recuperare. Nella tabella seguente sono elencati i valori che è possibile specificare per `lpValueName` . Si noti che per le stringhe valore non viene fatto distinzione tra maiuscole e minuscole.

|Valore|Descrizione
|-----|-----------
|`Global`| Recupera i dati sulle prestazioni per tutti gli oggetti prestazioni registrati nel computer, ad eccezione di quelli inclusi nella `Costly` categoria.
|`OLD_Global`| **Windows Vista e versioni successive:** Recupera i dati sulle prestazioni per tutti gli oggetti prestazioni **V1** registrati nel computer, ad eccezione di quelli inclusi nella `Costly` categoria. Usare questa opzione invece di evitare di raccogliere dati del provider V2 non necessari quando si è a sapere che i dati di interesse provengono `Global` da un provider V1.
|`n1 n2 ...`| Recupera i dati sulle prestazioni per uno o più oggetti prestazioni. Specificare l'indice decimale associato a ogni oggetto che si desidera recuperare in un elenco separato da spazi. Ad esempio, se si desidera recuperare gli oggetti System e Memory e si è determinato che gli indici delle stringhe di nome corrispondenti sono 2 e 4, specificare la stringa `"2 4"` . Si noti che la query può restituire un numero di oggetti diverso da quello richiesto. Ciò può verificarsi se l'oggetto specificato non è disponibile, se l'oggetto specificato dipende da un altro tipo di oggetto o se un provider restituisce in caso contrario dati che non sono stati richiesti direttamente. Ad esempio, i thread dipendono dai processi, quindi se si richiedono dati dall'oggetto , i risultati `Thread` includeranno i dati dell'oggetto `Process` .
|`Counter n`| Recupera le stringhe di nome per l'identificatore di lingua specificato, ad esempio l'inglese per `Counter 9` . Usare le stringhe dei nomi restituite per trovare l'indice corrispondente a un nome specificato o per trovare il nome corrispondente a un indice specificato. Per [informazioni dettagliate, vedere Recupero di nomi di contatori e testo della](retrieving-counter-names-and-help-text.md) Guida. Si noti che l'elenco restituito include sia i nomi degli oggetti (counterset) che i nomi dei contatori. Non esiste un modo semplice per determinare se un nome è un nome di oggetto o un nome di contatore.
|`Help n`| Recupera le stringhe della Guida per l'identificatore di lingua specificato, ad esempio l'inglese per `Help 9` . Usare le stringhe della Guida restituite per trovare le descrizioni corrispondenti agli indici dell'oggetto (counterset) o della Guida del contatore. Per [informazioni dettagliate, vedere Recupero di nomi di contatori e testo della](retrieving-counter-names-and-help-text.md) Guida.
|`Costly`| **Deprecato:** Recupera i dati sulle prestazioni per i tipi di oggetto i cui dati sono costosi da raccogliere in termini di tempo del processore o utilizzo della memoria. Questa raccolta può richiedere alcuni minuti in un computer con un carico molto grande. È consigliabile eseguire la raccolta in un thread di lavoro se l'applicazione deve rispondere all'utente durante la raccolta dei dati.

Per informazioni dettagliate sul formato dei dati sulle prestazioni restituiti dal Registro di sistema, vedere [Formato dei dati sulle prestazioni](performance-data-format.md).

Per un esempio che ottiene i nomi e le descrizioni dei contatori registrati nel computer, vedere Recupero di nomi di contatori [e testo della Guida](retrieving-counter-names-and-help-text.md).

Per un esempio che accede ai componenti dei dati sulle prestazioni, vedere Visualizzazione di nomi di [oggetti, istanze e contatori](displaying-object-instance-and-counter-names.md).

Per un esempio che recupera, calcola e stampa i valori dei contatori, vedere [Recupero](retrieving-counter-data.md) dei dati del contatore e [Calcolo dei valori dei contatori](calculating-counter-values.md).

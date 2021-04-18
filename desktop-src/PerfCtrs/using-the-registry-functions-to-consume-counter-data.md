---
description: È possibile utilizzare le funzioni del registro di sistema per raccogliere dati sulle prestazioni.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Utilizzo delle funzioni del registro di sistema per utilizzare i dati del contatore
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ce2a4ba9992510cb296b037cfd98965410c48939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312074"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Utilizzo delle funzioni del registro di sistema per utilizzare i dati del contatore

Utilizzare le [funzioni del registro](/windows/desktop/SysInfo/registry-functions) di sistema per raccogliere dati sulle prestazioni dalla `HKEY_PERFORMANCE_DATA` chiave del registro di sistema speciale.

I dati sulle prestazioni non vengono effettivamente archiviati nel registro di sistema. Chiamando le funzioni del registro di sistema, il sistema raccoglie i dati dal provider di dati prestazioni appropriato.

> [!Note]
> Le funzioni del registro di sistema non devono essere utilizzate normalmente per utilizzare i dati del contatore. È invece consigliabile [utilizzare le funzioni PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md). Le funzioni PDH sono più facili da usare ed evitano molti problemi di prestazioni e affidabilità che possono verificarsi tramite l'uso errato delle funzioni del registro di sistema.

> [!Note]
> Non è possibile usare le funzioni del registro di sistema se si scrivono app OneCore di Windows. Usare invece le [funzioni consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).

Le funzioni del registro di sistema sono l'API di basso livello per la raccolta dei dati dai **provider v1**. Le funzioni del registro di sistema supportano anche la raccolta dei dati dai **provider v2** tramite un livello di conversione che chiama le [funzioni consumer V2](using-the-perflib-functions-to-consume-counter-data.md).

Per ottenere i dati sulle prestazioni dal sistema locale, chiamare la funzione [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) . Utilizzare `HKEY_PERFORMANCE_DATA` come chiave. La prima chiamata apre la chiave. Non è necessario aprire prima la chiave in modo esplicito.

Per ottenere dati sulle prestazioni da un sistema remoto, chiamare la funzione [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) . Usare il nome computer del sistema remoto e usare `HKEY_PERFORMANCE_DATA` come chiave. Questa chiamata recupera una chiave che rappresenta i dati sulle prestazioni per il sistema remoto. Usare questa chiave invece di `HKEY_PERFORMANCE_DATA` Key per recuperare i dati.

Assicurarsi di usare la funzione [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) per chiudere l'handle alla chiave al termine del recupero dei dati sulle prestazioni. Questo è importante per i casi locali e remoti:

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` non chiude effettivamente un handle del registro di sistema, ma cancella tutti i dati memorizzati nella cache e libera le DLL delle prestazioni caricate.
- `RegCloseKey(hkeyRemotePerformanceData)` chiude l'handle al registro di sistema del computer remoto.

> [!IMPORTANT]
> Non chiamare `RegCloseKey(HKEY_PERFORMANCE_DATA)` durante `DLL_PROCESS_DETACH` .

Usare il `lpValueName` parametro della funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) per indicare le informazioni da recuperare. Nella tabella seguente sono elencati i valori che è possibile specificare per `lpValueName` . Si noti che le stringhe di valore non fanno distinzione tra maiuscole e minuscole.

|Valore|Descrizione
|-----|-----------
|`Global`| Recupera i dati sulle prestazioni per tutti gli oggetti prestazioni registrati nel computer, ad eccezione di quelli inclusi nella `Costly` categoria.
|`OLD_Global`| **Windows Vista e versioni successive:** Recupera i dati sulle prestazioni per tutti gli oggetti prestazioni **V1** registrati nel computer, ad eccezione di quelli inclusi nella `Costly` categoria. Usare questo valore anziché `Global` per evitare di raccogliere dati del provider v2 superflui quando si è certi che i dati di interesse provengono da un provider v1.
|`n1 n2 ...`| Recupera i dati sulle prestazioni per uno o più oggetti prestazione. Specificare l'indice decimale associato a ogni oggetto che si desidera recuperare in un elenco separato da spazi. Se ad esempio si desidera recuperare gli oggetti di sistema e di memoria e si è determinato che gli indici delle stringhe dei nomi corrispondenti sono 2 e 4, specificare la stringa `"2 4"` . Si noti che la query può restituire un numero di oggetti diverso da quello richiesto. Questo problema può verificarsi se l'oggetto specificato non è disponibile, se l'oggetto specificato dipende da un altro tipo di oggetto o se un provider restituisce dati non direttamente richiesti. Ad esempio, i thread dipendono dai processi, pertanto se si richiedono dati dall' `Thread` oggetto, i risultati includeranno i dati dell' `Process` oggetto.
|`Counter n`| Recupera le stringhe di nome per l'identificatore di lingua specificato, ad esempio l'inglese per `Counter 9` . Utilizzare le stringhe nome restituite per trovare l'indice corrispondente a un determinato nome o per trovare il nome corrispondente a un indice specificato. Per informazioni dettagliate, vedere [recupero dei nomi dei contatori e del testo della Guida](retrieving-counter-names-and-help-text.md) . Si noti che nell'elenco restituito sono inclusi sia i nomi di oggetto (contatore) che i nomi dei contatori, non esiste un modo semplice per determinare se un nome è un nome di oggetto o un nome di contatore.
|`Help n`| Recupera le stringhe della Guida per l'identificatore di lingua specificato, ad esempio l'inglese per `Help 9` . Utilizzare le stringhe della Guida restituite per trovare le descrizioni corrispondenti agli indici dell'oggetto (contatore) o della guida del contatore. Per informazioni dettagliate, vedere [recupero dei nomi dei contatori e del testo della Guida](retrieving-counter-names-and-help-text.md) .
|`Costly`| **Deprecato:** Recupera i dati sulle prestazioni per i tipi di oggetto i cui dati sono costosi da raccogliere in termini di tempo del processore o utilizzo della memoria. Questa raccolta può richiedere alcuni minuti in un computer molto caricato. È consigliabile eseguire la raccolta in un thread di lavoro se l'applicazione deve rispondere all'utente durante la raccolta dei dati.

Per informazioni dettagliate sul formato dei dati sulle prestazioni restituiti dal registro di sistema, vedere [formato dei dati sulle prestazioni](performance-data-format.md).

Per un esempio in cui vengono ottenuti i nomi e le descrizioni dei contatori registrati nel computer, vedere [recupero di nomi di contatori e testo della Guida](retrieving-counter-names-and-help-text.md).

Per un esempio di accesso ai componenti dei dati sulle prestazioni, vedere [visualizzazione di nomi di oggetti, istanze e contatori](displaying-object-instance-and-counter-names.md).

Per un esempio in cui vengono recuperati, calcolati e stampati i valori dei contatori, vedere [recupero di dati del contatore](retrieving-counter-data.md) e calcolo dei valori dei [contatori](calculating-counter-values.md).

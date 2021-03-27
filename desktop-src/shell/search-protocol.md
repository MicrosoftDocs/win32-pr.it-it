---
description: "La ricerca: il protocollo applicativo è una convenzione estendibile per chiamare l'applicazione di ricerca desktop in Windows Vista con Service Pack 1 (SP1) e versioni successive."
title: Uso del protocollo di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995029"
---
# <a name="using-the-search-protocol"></a>Uso del protocollo di ricerca

La **ricerca:** il [protocollo applicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) è una convenzione estendibile per chiamare l'applicazione di ricerca desktop in Windows Vista con Service Pack 1 (SP1) e versioni successive. Il protocollo è stato creato in Windows Vista con SP1 (per informazioni, vedere la panoramica dell'articolo della Knowledge Base relativo alle [modifiche di ricerca desktop di Windows Vista in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) per consentire a Windows di determinare e chiamare l'applicazione di ricerca desktop predefinita.

La sintassi del protocollo fornisce una serie di parametri utili per eseguire ricerche comuni sui desktop, ad esempio i termini di ricerca immessi dall'utente o il percorso in cui è stata avviata la ricerca. Quando gli utenti effettuano la ricerca da uno dei due punti di ingresso di ricerca disponibili, ovvero dal menu **Start** o da Esplora risorse, il sistema operativo usa il protocollo di ricerca per avviare l'applicazione di ricerca desktop predefinita. Questa operazione viene eseguita aggiungendo i termini di ricerca immessi dall'utente alla sintassi del protocollo di ricerca standard e passando le informazioni all'applicazione registrata come applicazione di ricerca predefinita.

Se non sono installate altre applicazioni di ricerca desktop, una ricerca immessa in questi punti di ingresso avvia Esplora ricerche di Windows. Tuttavia, gli sviluppatori di terze parti possono creare, installare e registrare le proprie applicazioni per gestire il protocollo di ricerca e l'applicazione di ricerca predefinita. Tali applicazioni devono supportare la sintassi del protocollo di ricerca ed eseguire la registrazione con la funzionalità [programmi predefiniti](default-programs.md) per garantire un'esperienza senza problemi con Windows.

Se si sviluppa un'applicazione destinata all'utilizzo o alla compilazione di un'applicazione di ricerca desktop specifica, è consigliabile non basarsi esclusivamente sul protocollo **Search:** . Poiché molte applicazioni possono essere proprietarie del protocollo **Search:** , non c'è alcuna garanzia che l'applicazione di ricerca desktop di destinazione ne sarà proprietaria in un determinato momento. È invece consigliabile usare un protocollo di ricerca privato definito da tale applicazione di ricerca desktop di destinazione. Ciò significa che le applicazioni di ricerca desktop destinate a essere una piattaforma per le applicazioni di terze parti devono supportare sia il protocollo **Search:** che il protocollo di ricerca proprietario.

> [!Note]  
> Il protocollo **Search:** non sostituisce il protocollo di [ricerca proprietario-MS:](../search/-search-3x-wds-qryidx-searchms.md) . Le applicazioni possono comunque usare il protocollo **search-ms:** per avviare Esplora ricerche finestre o per eseguire una query in modo invisibile all'indicizzatore di ricerca di Windows.

 

Questo argomento illustra quanto segue:

-   [Sintassi](#syntax)
-   [Windows Vista con SP1 utilizzo del protocollo di ricerca:](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [esempi](#examples)
-   [Registrazione dell'applicazione che gestisce il protocollo](#registering-the-application-that-handles-the-protocol)
    -   [Voci del registro di sistema](#registry-entries)
-   [Argomenti correlati](#related-topics)

## <a name="syntax"></a>Sintassi

Il protocollo di ricerca usa la sintassi standard codificata con URL seguente:


```C++
search:parameter=value[&parameter=value]&
```



La sintassi inizia identificando il protocollo stesso (**Search:**). Le coppie parametro/valore sono argomenti passati al motore di ricerca, come descritto nella tabella seguente, che Mostra tutti i parametri possibili per la sintassi del protocollo di ricerca.



| Parametro                                              | Valore                                                         | Descrizione                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| query                                                  | Testo con codifica URL                                              | Testo della query immesso dall'utente.                                                                                                                                                                                                                                                            |
| [InputLocale](search-protocol-localeidentifiers.md)   | Qualsiasi identificatore di codice lingua (LCID) valido                     | Identificatore LCID che identifica la lingua di input per la query.                                                                                                                                                                                                                                     |
| [keywordlocale](search-protocol-localeidentifiers.md) | Qualsiasi LCID valido                                                | Identificatore LCID che identifica la lingua della versione internazionale dell'indicizzatore. Il valore predefinito è 1033 (en-US).                                                                                                                                                                                |
| [navigazione](search-protocol-crumb.md)                     | AQS-istruzione                                                 | Questo argomento limita l'ambito di ricerca. In Windows Vista il protocollo di ricerca supporta AQS completi e un'implementazione speciale per un `location` argomento. In Windows XP il protocollo di ricerca supporta anche AQS completi, ad eccezione di una speciale implementazione di `kind` e `store` . |
| [sintassi](search-protocol-syntaxargument.md)           | NQS, AQS (senza distinzione tra maiuscole e minuscole)                                 | Sintassi di query da utilizzare per la ricerca nell'indice: la sintassi di query naturale o la sintassi di query avanzata (AQS). AQS è l'impostazione predefinita e viene sempre utilizzata come analizzata e supportata.                                                                                                                        |
| [stackedby](search-protocol-stackedby.md)             | Qualsiasi proprietà valida del sistema di proprietà                   | Proprietà che specifica la colonna in base alla quale eseguire lo stack dei risultati.                                                                                                                                                                                                                                      |
| [subquery](search-protocol-subquery.md)               | Percorso specificato completamente per un file di ricerca salvato ( \* . search-ms) | I risultati della sottoquery vengono utilizzati come origine per la query. Ovvero i termini della query vengono cercati in base ai risultati della sottoquery.                                                                                                                                               |
| displayname                                            | Stringa con codifica URL                                            | Nome della ricerca corrente.                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a>Windows Vista con SP1 utilizzo del protocollo di ricerca:

Windows Vista con SP1 include diversi punti di ingresso da cui viene chiamato il protocollo **Search:** . Questi punti di ingresso sono descritti sotto, oltre alla sintassi comune associata a ognuno di essi.



| Cerca punto di ingresso del protocollo | Location         | Query chiamata                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| **Cerca in tutto il mondo**       | Menu **Start**   | ricerca: query = *termine di ricerca*<>                                   |
| **Cerca in tutto il mondo**       | Esplora risorse | ricerca: query =<*termine di ricerca*>&briciolo = posizione: <*località*> |
| Tasto logo Windows+F          | Ovunque         | ricerca                                                              |
| CTRL+F                      | Esplora risorse | ricerca: query =<*termine di ricerca*>&briciolo = posizione: <*località*> |
| F3                          | Menu **Start**   | ricerca                                                              |
| F3                          | Esplora risorse | ricerca: query =<*termine di ricerca*>&briciolo = posizione: <*località*> |



 

I punti di ingresso del protocollo di ricerca di Windows Vista con SP1 non sfruttano tutti i possibili parametri nel protocollo di ricerca. Le applicazioni che riguardano solo la gestione delle chiamate del protocollo di ricerca da Windows Vista con SP1 possono utilizzare la tabella seguente come guida al valore minimo necessario per l'implementazione.



| Parametro                                              | Usato da Windows? | Modalità di utilizzo di Windows Vista con SP1 durante la chiamata alla ricerca:                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| query                                                  | Sì              | Testo della query immesso dall'utente.                                                                                                                                                                                                                                         |
| [navigazione](search-protocol-crumb.md)                     | Sì              | [briciola](search-protocol-crumb.md) usa l' `location` argomento per specificare da dove proviene la query.                                                                                                                                                                       |
| [subquery](search-protocol-subquery.md)               | Sì              | I risultati dell'argomento [sottoquery](search-protocol-subquery.md) vengono utilizzati come ambito degli elementi in cui eseguire la ricerca. Questa operazione viene in genere usata se un utente usa un file. search-ms per eseguire la ricerca e quindi chiama l'applicazione di ricerca desktop predefinita dall'interno di tale ricerca. |
| [InputLocale](search-protocol-localeidentifiers.md)   | No               | Attualmente non utilizzato.                                                                                                                                                                                                                                                         |
| [keywordlocale](search-protocol-localeidentifiers.md) | No               | Attualmente non utilizzato.                                                                                                                                                                                                                                                         |
| [sintassi](search-protocol-syntaxargument.md)           | No               | Attualmente non utilizzato.                                                                                                                                                                                                                                                         |
| [stackedby](search-protocol-stackedby.md)             | No               | Attualmente non utilizzato.                                                                                                                                                                                                                                                         |
| displayname                                            | No               | Attualmente non utilizzato.                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a>Esempio

Se un utente immette "Microsoft" nel menu **Start** e fa clic su **Cerca ovunque**, viene effettuata la chiamata al protocollo di ricerca risultante:


```C++
search:query=microsoft&
```



Se un utente immette "Seattle" in Esplora risorse all'interno di C: \\ cartella e quindi fa clic su **Cerca ovunque**, viene eseguita la chiamata seguente, usando i caratteri di escape per ":" e " \\ ":


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a>Registrazione dell'applicazione che gestisce il protocollo

Poiché più applicazioni possono sostenere il protocollo di ricerca, è necessario registrare l'applicazione con la funzionalità [programmi predefiniti](default-programs.md) durante l'installazione per consentire all'utente di configurare più facilmente il valore predefinito. Oltre alle procedure di installazione normalmente disponibili in Windows XP, un'applicazione basata su Windows Vista deve eseguire la registrazione con la funzionalità programmi predefiniti, in modo che l'applicazione e gli utenti possano configurare facilmente le impostazioni predefinite.

Dopo aver installato i file binari necessari nel computer dell'utente, la routine di installazione deve completare le attività generali seguenti:

1.  Scrivere i ProgID nel **\_ \_ computer locale HKEY**, come descritto di seguito. Si noti che le applicazioni devono creare ProgID specifici dell'applicazione per il protocollo di ricerca.
2.  Associazione del protocollo di ricerca a livello di computer Claim.
3.  Registrare l'applicazione con i [programmi predefiniti](default-programs.md), come illustrato in [registrazione di un'applicazione per l'utilizzo con i programmi predefiniti](default-programs.md), come un contendente per il protocollo di ricerca.

### <a name="registry-entries"></a>Voci del Registro di sistema

Di seguito sono riportati alcuni esempi delle voci del registro di sistema necessarie per un'applicazione di ricerca desktop fittizia, contoso search.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi di ricerca avanzata](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> </dl>

 

 

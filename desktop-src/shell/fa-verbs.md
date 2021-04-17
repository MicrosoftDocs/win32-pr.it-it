---
description: Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, ad esempio un file, la shell Visualizza un menu di scelta rapida (contesto).
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verbi e associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b398b168afe66c3ddd1abe4c78863fbf67ffcbd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558918"
---
# <a name="verbs-and-file-associations"></a>Verbi e associazioni di file

Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, ad esempio un file, la shell Visualizza un menu di scelta rapida (contesto). Questo menu contiene un elenco di comandi che l'utente può selezionare per eseguire varie azioni sull'elemento. Questi comandi sono noti anche come voci di menu di scelta rapida o verbi. È possibile personalizzare i menu di scelta rapida.

Questo argomento è organizzato nel modo seguente:

-   [Introduzione ai menu di scelta rapida per gli oggetti del file System](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Aggiungere comandi a un menu di scelta rapida](#add-commands-to-a-shortcut-menu)
-   [Verbi del menu di scelta rapida](#shortcut-menu-verbs)
-   [Trasmettere gli elementi non del file System e i risultati di OpenSearch.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrare un'applicazione per gestire i tipi di file arbitrari](#register-an-application-to-handle-arbitrary-file-types)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Introduzione ai menu di scelta rapida per gli oggetti del file System

Poiché i menu di scelta rapida vengono spesso utilizzati per la gestione dei file, la shell fornisce un set di comandi predefiniti, ad esempio **taglia** e **copia**, che vengono visualizzati nel menu di scelta rapida per qualsiasi file System oggetto, ad esempio un file o una cartella.

Nell'esempio seguente viene illustrato un menu di scelta rapida predefinito visualizzato facendo clic con il pulsante destro del mouse su **MyFile.xyz-MS**.

![screenshot del menu di scelta rapida predefinito](images/context-menu/context-filesystemobjects.png)

Il motivo per cui viene visualizzato un menu di scelta rapida predefinito per **MyFile.xyz-MS** è dovuto al fatto che **. xyz-MS** non è un membro di un tipo di file registrato. Al contrario, **txt** è un tipo di file registrato. Se si fa clic con il pulsante destro del mouse su un file con **estensione txt** , nella sezione superiore verrà visualizzato un menu di scelta rapida con tre comandi aggiuntivi, ovvero **stampa**, **modifica** e **Apri con**.

![screenshot del menu di scelta rapida per un file con un tipo di file registrato](images/context-menu/context-registeredfiletype.png)

Per estendere il menu di scelta rapida per un tipo di file, è necessario creare una voce del registro di sistema per ogni comando. Un approccio più sofisticato consiste nell'implementare un gestore di menu di scelta rapida (verbo), che consente di estendere il menu di scelta rapida per un tipo di file in base al file. Per altre informazioni, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md)e [riferimento al menu di scelta rapida](context-menu-reference.md).

### <a name="add-commands-to-a-shortcut-menu"></a>Aggiungere comandi a un menu di scelta rapida

Un gestore di menu di scelta rapida è un gestore di tipi di file che aggiunge comandi a un menu di scelta rapida esistente. I gestori dei menu di scelta rapida sono associati a un tipo di file e vengono chiamati ogni volta che viene visualizzato un menu di scelta rapida per un membro della classe. La shell controlla il registro di sistema per verificare se il tipo di file è associato a qualsiasi gestore di menu di scelta rapida. In caso contrario, la shell esegue una query sui gestori per altre voci di menu di scelta rapida.

## <a name="shortcut-menu-verbs"></a>Verbi del menu di scelta rapida

Ogni comando nel menu di scelta rapida viene identificato nel registro di sistema in base al relativo verbo. Questi verbi corrispondono a quelli usati da [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) quando si avviano le applicazioni a livello di codice.

Un verbo è una stringa di testo semplice utilizzata dalla Shell per identificare il comando associato. Ogni verbo corrisponde alla stringa di comando usata per avviare il comando in una finestra della console o in un file batch (. bat).

Il verbo Open, ad esempio, avvia normalmente un programma per aprire un file. La stringa di comando è in genere simile alla seguente:


```
"My Program.exe" "%1"
```



Se un elemento della stringa di comando contiene o potrebbe contenere spazi, deve essere racchiuso tra virgolette. In caso contrario, se l'elemento contiene uno spazio, non verrà analizzato correttamente. Ad esempio, **"My Program.exe"** avvia correttamente l'applicazione. Se si utilizza **my Program.exe** senza virgolette, il sistema tenta di avviare **My** con **Program.exe** come primo argomento della riga di comando. È consigliabile utilizzare sempre le virgolette con argomenti, ad esempio **"%1**", che vengono espanse in stringhe dalla shell, perché non è possibile essere certi che la stringa non conterrà uno spazio.

Ai verbi può essere associato anche un nome visualizzato, che viene visualizzato nel menu di scelta rapida anziché nella stringa del verbo. La stringa di visualizzazione per opens, ad esempio, è **aperta con**. Analogamente alle normali stringhe di menu, incluso un carattere e commerciale nella stringa di visualizzazione consente la selezione del comando da tastiera.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>Trasmettere gli elementi non del file System e i risultati di OpenSearch.

In Windows 7 e versioni successive, è disponibile il supporto per la connessione di origini esterne al client Windows tramite il protocollo [OpenSearch](http://www.opensearch.org/) . Ciò consente agli utenti di eseguire ricerche in un archivio dati remoto e visualizzare i risultati da Esplora risorse. Lo standard OpenSearch v 1.1 definisce formati di file semplici che possono essere utilizzati per descrivere il modo in cui un client deve eseguire una query sul servizio Web per l'archivio dati e il modo in cui il servizio deve restituire i risultati per il rendering da parte del client.

Potrebbe essere necessario eseguire lo streaming di elementi non file system per evitare la necessità di scaricare elementi nel caso di risultati di [OpenSearch](http://www.opensearch.org/) . La funzionalità di ricerca federata consente la ricerca di elementi da posizioni non file system che supportano OpenSearch, ad esempio SharePoint e altri siti supportati da servizi Web. Quando si richiamano i verbi su questi elementi, il sistema Scarica una versione temporanea dell'elemento e la passa all'implementazione del verbo. Gli implementatori di verbi sono invitati a evitare la necessità di scaricare il file registrando il set di schemi URL supportati dal verbo per trasmettere gli elementi. I verbi lo eseguono usando la chiave del registro di sistema **SupportedProtocols: Recupera** .

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrare un'applicazione per gestire i tipi di file arbitrari

La definizione di voci di menu di scelta rapida per un determinato tipo di file consente di specificare il modo in cui l'applicazione associata apre un membro del tipo di file. Tuttavia, le applicazioni possono anche registrare una procedura predefinita separata da usare quando un utente tenta di usare l'applicazione per aprire un tipo di file non associato all'applicazione. Registrare la procedura predefinita nello stesso modo in cui si registrano le voci di menu di scelta rapida. Per informazioni più dettagliate sulla definizione di voci di menu di scelta rapida, vedere [creazione di gestori di menu](context-menu.md)di scelta rapida.

La procedura predefinita si serve di due scopi di base. Uno consiste nel specificare come richiamare l'applicazione per aprire un tipo di file arbitrario. È possibile, ad esempio, usare un flag della riga di comando per indicare che è in corso l'apertura di un tipo di file sconosciuto. L'altro scopo è quello di definire le varie caratteristiche di un tipo di file, ad esempio le voci del menu di scelta rapida e l'icona. Se un utente associa l'applicazione a un tipo di file aggiuntivo, tale classe avrà queste caratteristiche. Se il tipo di file aggiuntivo è stato precedentemente associato a un'altra applicazione, tali caratteristiche sostituiranno quelle originali.

Per registrare la procedura predefinita, inserire le stesse chiavi del registro di sistema create per il ProgID dell'applicazione nella sottochiave dell'applicazione delle **\_ \_ \\ applicazioni radice delle classi HKEY**. È anche possibile includere un valore **FriendlyAppName** per fornire al sistema un nome descrittivo per l'applicazione. Il nome descrittivo dell'applicazione può essere estratto anche dal file eseguibile, ma solo se il valore FriendlyAppName è assente.

Nella voce del registro di sistema di esempio seguente viene illustrata una procedura predefinita per **MyProgram.exe** che definisce un nome descrittivo e varie voci di menu di scelta rapida. Le stringhe di comando includono il flag **/a** per notificare all'applicazione che sta aprendo un tipo di file arbitrario. Se si include una sottochiave **DefaultIcon** , è consigliabile usare un'icona generica.

```
HKEY_CLASSES_ROOT
   MyProgram.exe
      shell
         open
            command
               (Default) = C:\MyDir\MyProgram.exe /a "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2"
```

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per ulteriori informazioni, vedere [Introduzione alle associazioni di file](fa-intro.md).
-   Per informazioni concettuali sull'estensione della shell con gestori di tipi di file, vedere [creazione di gestori di estensioni della shell](handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per i gestori di menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida (contesto) e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Riferimento al menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 




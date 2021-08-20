---
description: Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, ad esempio un file, shell visualizza un menu di scelta rapida.
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verbi e associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a144051b04ef2d9a2c9877b53e1680d4274afc92d3fc87fbcb531b02a0f94946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860788"
---
# <a name="verbs-and-file-associations"></a>Verbi e associazioni di file

Quando un utente fa clic con il pulsante destro del mouse su un oggetto Shell, ad esempio un file, shell visualizza un menu di scelta rapida. Questo menu contiene un elenco di comandi che l'utente può selezionare per eseguire varie azioni sull'elemento. Questi comandi sono noti anche come voci di menu di scelta rapida o verbi. I menu di scelta rapida possono essere personalizzati.

Questo argomento è organizzato come segue:

-   [Introduzione ai menu di scelta rapida per gli oggetti del file system](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Aggiungere comandi a un menu di scelta rapida](#add-commands-to-a-shortcut-menu)
-   [Verbi del menu di scelta rapida](#shortcut-menu-verbs)
-   [Trasmettere elementi non del file system e OpenSearch risultati.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrare un'applicazione per gestire tipi di file arbitrari](#register-an-application-to-handle-arbitrary-file-types)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Introduzione ai menu di scelta rapida per gli oggetti del file system

Poiché i menu di scelta rapida vengono spesso usati per la gestione dei file, Shell fornisce un set di comandi predefiniti, ad esempio **Taglia** e Copia **,** che vengono visualizzati nel menu di scelta rapida per qualsiasi oggetto file system, ad esempio un file o una cartella.

L'esempio seguente illustra un menu di scelta rapida predefinito visualizzato facendo clic con il pulsante destro del mouse **MyFile.xyz-ms**.

![Screenshot del menu di scelta rapida predefinito](images/context-menu/context-filesystemobjects.png)

Il motivo per cui viene visualizzato un menu di scelta rapida predefinito **per MyFile.xyz-ms** è dovuto al fatto che **.xyz-ms** non è un membro di un tipo di file registrato. Al contrario, **.txt** è un tipo di file registrato. Se si fa clic con il pulsante **destro del** mouse su un file di.txt, viene visualizzato un menu di scelta rapida con tre comandi aggiuntivi nella sezione superiore: **Stampa** **,** Modifica **e Apri con**.

![Screenshot del menu di scelta rapida per un file con un tipo di file registrato](images/context-menu/context-registeredfiletype.png)

Per estendere il menu di scelta rapida per un tipo di file, è necessario creare una voce del Registro di sistema per ogni comando. Un approccio più sofisticato consiste nell'implementare un gestore di menu di scelta rapida (verbo), che consente di estendere il menu di scelta rapida per un tipo di file per ogni file. Per altre informazioni, vedere [Creazione di gestori del menu di scelta rapida](context-menu-handlers.md)e Informazioni di riferimento sul menu di scelta [rapida.](context-menu-reference.md)

### <a name="add-commands-to-a-shortcut-menu"></a>Aggiungere comandi a un menu di scelta rapida

Un gestore del menu di scelta rapida è un gestore di tipi di file che aggiunge comandi a un menu di scelta rapida esistente. I gestori del menu di scelta rapida sono associati a un tipo di file e vengono chiamati ogni volta che viene visualizzato un menu di scelta rapida per un membro della classe . Shell controlla il Registro di sistema per verificare se il tipo di file è associato a qualsiasi gestore del menu di scelta rapida. In caso contrario, Shell esegue una query nei gestori per altre voci del menu di scelta rapida.

## <a name="shortcut-menu-verbs"></a>Verbi del menu di scelta rapida

Ogni comando del menu di scelta rapida viene identificato nel Registro di sistema dal verbo. Questi verbi sono gli stessi usati da [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) quando si avviano applicazioni a livello di codice.

Un verbo è una stringa di testo semplice usata da Shell per identificare il comando associato. Ogni verbo corrisponde alla stringa di comando usata per avviare il comando in una finestra della console o in un file batch (.bat).

Ad esempio, il verbo open in genere avvia un programma per aprire un file. La stringa di comando è in genere simile alla seguente:


```
"My Program.exe" "%1"
```



Se un elemento della stringa di comando contiene o può contenere spazi, deve essere racchiuso tra virgolette. In caso contrario, se l'elemento contiene uno spazio, non verrà analizzato correttamente. Ad esempio, **"My Program.exe"** avvia correttamente l'applicazione. Se si usa **My Program.exe** senza virgolette, il sistema tenta di avviare **My** **conProgram.exe** come primo argomento della riga di comando. È consigliabile usare sempre le virgolette con argomenti come **"%1"** espansi in stringhe da Shell, perché non è possibile essere certi che la stringa non conterrà uno spazio.

Ai verbi può essere associato anche un nome visualizzato, che viene visualizzato nel menu di scelta rapida anziché nella stringa del verbo. Ad esempio, la stringa di visualizzazione per openas è **Open With**. Analogamente alle normali stringhe di menu, l'inclusione di un carattere e commerciale nella stringa di visualizzazione consente la selezione da tastiera del comando.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>Trasmettere elementi non del file system e OpenSearch risultati.

In Windows 7 e versioni successive è disponibile il supporto della connessione di origini esterne al client Windows tramite il protocollo [OpenSearch.](http://www.opensearch.org/) In questo modo gli utenti possono eseguire ricerche in un archivio dati remoto e visualizzare i risultati dall'Windows Explorer. Lo standard OpenSearch v1.1 definisce formati di file semplici che possono essere usati per descrivere il modo in cui un client deve eseguire query sul servizio Web per l'archivio dati e come il servizio deve restituire risultati per il rendering da parte del client.

Potrebbe essere necessario trasmettere elementi non file system per evitare la necessità di scaricare elementi in caso di OpenSearch [risultati.](http://www.opensearch.org/) La funzionalità di ricerca federata consente la ricerca di elementi da posizioni non file system che supportano OpenSearch, ad esempio SharePoint e altri siti supportati da servizi Web. Quando si richiamano verbi su questi elementi, il sistema scarica una versione temporanea dell'elemento e la passa all'implementazione del verbo. Gli implementatori di verbi sono invitati a evitare la necessità di scaricare il file registrando il set di schemi URL supportati dal verbo per trasmettere gli elementi. A tale scopo, i verbi usano la chiave del Registro di **sistema SupportedProtocols.**

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrare un'applicazione per gestire tipi di file arbitrari

La definizione di voci di menu di scelta rapida per un particolare tipo di file consente di specificare la modalità di apertura di un membro del tipo di file da parte dell'applicazione associata. Tuttavia, le applicazioni possono anche registrare una procedura predefinita separata da usare quando un utente tenta di usare l'applicazione per aprire un tipo di file non associato all'applicazione. La procedura predefinita viene registrare in modo molto identico a come si registrano le voci del menu di scelta rapida. Per informazioni più dettagliate sulla definizione delle voci di menu di scelta rapida, vedere [Creazione di gestori del menu di scelta rapida.](context-menu.md)

La procedura predefinita ha due scopi di base. Uno è specificare come richiamare l'applicazione per aprire un tipo di file arbitrario. È ad esempio possibile usare un flag della riga di comando per indicare che è in corso l'apertura di un tipo di file sconosciuto. L'altro scopo è definire le varie caratteristiche di un tipo di file, ad esempio le voci del menu di scelta rapida e l'icona. Se un utente associa l'applicazione a un tipo di file aggiuntivo, tale classe avrà queste caratteristiche. Se il tipo di file aggiuntivo è stato precedentemente associato a un'altra applicazione, queste caratteristiche sostituiranno gli originali.

Per registrare la procedura predefinita, inserire le stesse chiavi del Registro di sistema create per ProgID dell'applicazione nella sottochiave dell'applicazione **HKEY \_ CLASSES ROOT \_ \\ Applications**. È anche possibile includere un **valore FriendlyAppName** per fornire al sistema un nome descrittivo per l'applicazione. Il nome descrittivo dell'applicazione può anche essere estratto dal file eseguibile, ma solo se il valore FriendlyAppName è assente.

La voce del Registro di sistema di esempio seguente illustra una procedura predefinita perMyProgram.exe **che** definisce un nome descrittivo e diverse voci di menu di scelta rapida. Le stringhe di comando includono il flag **/a** per notificare all'applicazione che sta aprendo un tipo di file arbitrario. Se si include una **sottochiave DefaultIcon,** è consigliabile usare un'icona generica.

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

-   Per altre informazioni, vedere [Introduzione alle associazioni di file](fa-intro.md).
-   Per informazioni concettuali sull'estensione della shell con gestori di tipi di file, vedere [Creazione di gestori di estensioni della shell](handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per i gestori del menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Informazioni di riferimento sul menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 




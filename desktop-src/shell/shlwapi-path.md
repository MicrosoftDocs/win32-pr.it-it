---
description: In questa sezione vengono descritte le Windows di gestione dei percorsi della shell. Gli elementi di programmazione illustrati in questa documentazione vengono esportati Shlwapi.dll e definiti in Shlwapi.h e Shlwapi.lib.
title: Funzioni di gestione del percorso della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ab485d7055ed6412698d06e9d95628074c85f3cc1e7ac52e7513dd8975529826
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111121"
---
# <a name="shell-path-handling-functions"></a>Funzioni di gestione del percorso della shell

In questa sezione vengono descritte le Windows di gestione dei percorsi della shell. Gli elementi di programmazione illustrati in questa documentazione vengono esportati Shlwapi.dll e definiti in Shlwapi.h e Shlwapi.lib.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a><br/></td>
<td>Aggiunge una barra rovesciata alla fine di una stringa per creare la sintassi corretta per un percorso. Se il percorso di origine ha già una barra rovesciata finale, non verrà aggiunta alcuna barra rovesciata. <br/>
<blockquote>
[!Note]<br />
L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> più sicura.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a><br/></td>
<td>Aggiunge un'estensione di file a una stringa di percorso.<br/>
<blockquote>
[!Note]<br />
L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>la funzione PathCchAddExtension</strong></a> più sicura.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a><br/></td>
<td>Aggiunge un percorso alla fine di un altro. <br/>
<blockquote>
[!Note]<br />
L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> più sicura.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a><br/></td>
<td>Crea un percorso radice da un numero di unità specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a><br/></td>
<td>Semplifica un percorso rimuovendo gli elementi di navigazione, ad esempio . e .. per produrre un percorso diretto &quot; &quot; e ben &quot; &quot; formato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a><br/></td>
<td>Concatena due stringhe che rappresentano percorsi correttamente formati in un unico percorso. concatena anche tutti gli elementi del percorso relativo. <br/>
<blockquote>
[!Note]<br />
L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> più sicura.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a><br/></td>
<td>Confronta due percorsi per determinare se condividono un prefisso comune. Un prefisso è uno dei tipi seguenti: &quot; C: \\ &quot; , . , . . &quot; . . . &quot; &quot; &quot; &quot; \\ &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a><br/></td>
<td>Tronca un percorso di file in base a una larghezza in pixel specificata sostituendo i componenti del percorso con puntini di sospensione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a><br/></td>
<td>Tronca un tracciato per rientrare in un determinato numero di caratteri sostituendo i componenti del tracciato con puntini di sospensione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br/></td>
<td>Converte l'URL di un file in un percorso Microsoft MS-DOS.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br/></td>
<td>Crea un percorso da un URL di file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a><br/></td>
<td>Determina se un percorso di un file system, ad esempio un file o una cartella, è valido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a><br/></td>
<td>Cerca un'estensione in un percorso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a><br/></td>
<td>Cerca un nome file in un percorso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br/></td>
<td>Analizza un percorso e restituisce la parte di tale percorso che segue la prima barra rovesciata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br/></td>
<td>Cerca un file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br/></td>
<td>Determina se un nome di file specificato ha uno di un elenco di suffissi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br/></td>
<td>Trova gli argomenti della riga di comando all'interno di un percorso specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br/></td>
<td>Determina il tipo di carattere in relazione a un percorso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a><br/></td>
<td>Cerca in un percorso una lettera di unità nell'intervallo da "A" a "Z" e restituisce il numero di unità corrispondente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br/></td>
<td>Determina se il tipo di contenuto registrato di un file corrisponde al tipo di contenuto specificato. Questa funzione ottiene il tipo di contenuto per il tipo di file specificato e confronta tale stringa con <em>pszContentType</em>. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a><br/></td>
<td>Verifica che un percorso sia una directory valida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br/></td>
<td>Determina se un percorso specificato è una directory vuota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br/></td>
<td>Cerca in un percorso tutti i caratteri di delimitazione del percorso ,ad esempio ':' o \' '. Se non sono presenti caratteri di delimitazione del percorso, il percorso viene considerato un percorso di specifica file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br/></td>
<td>Determina se un file è un file HTML. La determinazione viene effettuata in base al tipo di contenuto registrato per l'estensione del file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br/></td>
<td>Determina se un nome file è in formato lungo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br/></td>
<td>Determina se una stringa di percorso rappresenta una risorsa di rete.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a><br/></td>
<td>Cerca in un percorso per determinare se contiene un prefisso valido del tipo passato da <em>pszPrefix</em>. Un prefisso è uno dei tipi seguenti: &quot; C: \\ &quot; , . , . . &quot; . . . &quot; &quot; &quot; &quot; \\ &quot; .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a><br/></td>
<td>Cerca un percorso e determina se è relativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a><br/></td>
<td>Determina se una stringa di percorso fa riferimento alla radice di un volume.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a><br/></td>
<td>Confronta due percorsi per determinare se hanno un componente radice comune.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br/></td>
<td>Determina se una cartella esistente contiene gli attributi che la rendono una cartella di sistema. In alternativa, questa funzione indica se determinati attributi qualificano una cartella come cartella di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a><br/></td>
<td>Determina se una stringa di percorso è un percorso Universal Naming Convention (UNC) valido, anziché un percorso basato su una lettera di unità.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a><br/></td>
<td>Determina se una stringa è un UNC valido solo per un percorso del server.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a><br/></td>
<td>Determina se una stringa è un percorso di condivisione UNC valido, \\ <em>condivisione</em> \ <em>server</em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br/></td>
<td>Verifica una determinata stringa per determinare se è conforme a un formato URL valido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br/></td>
<td>Converte un percorso tutto maiuscolo in tutti i caratteri minuscoli per assegnare al percorso un aspetto coerente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br/></td>
<td>Fornisce a una cartella esistente gli attributi adeguati per diventare una cartella di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br/></td>
<td>Cerca una stringa usando un tipo di corrispondenza con caratteri jolly MS-DOS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br/></td>
<td>Trova la corrispondenza di un nome di file da un percorso rispetto a uno o più modelli di nome file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PercorsoParseIconLocation</strong></a><br/></td>
<td>Analizza una stringa di percorso del file che contiene un percorso di file e un indice di icona e restituisce valori separati.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br/></td>
<td>Cerca spazi in un percorso. Se vengono trovati spazi, l'intero percorso è racchiuso tra virgolette.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a><br/></td>
<td>Crea un percorso relativo da un file o una cartella a un altro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a><br/></td>
<td>Rimuove tutti gli argomenti da un percorso specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a><br/></td>
<td>Rimuove la barra rovesciata finale da un percorso specificato.<br/>
<blockquote>
[!Note]<br />
Questa funzione è deprecata. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a><br/></td>
<td>Rimuove tutti gli spazi iniziali e finali da una stringa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a><br/></td>
<td>Rimuove l'estensione di file da un percorso, se presente. <br/>
<blockquote>
[!Note]<br />
Questa funzione è deprecata. È consigliabile usare <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> al suo posto.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a><br/></td>
<td>Rimuove il nome file finale e la barra rovesciata da un percorso, se presenti.<br/>
<blockquote>
[!Note]<br />
Questa funzione è deprecata. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br/></td>
<td>Sostituisce l'estensione di un nome file con una nuova estensione. Se il nome file non contiene un'estensione, l'estensione verrà allegata alla fine della stringa.<br/>
<blockquote>
[!Note]<br />
L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> più sicura.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br/></td>
<td>Determina se un percorso specificato è formattato correttamente e completo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br/></td>
<td>Imposta il testo di un controllo figlio in una finestra o in una finestra di dialogo, usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> per garantire che il percorso si adatti al controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a><br/></td>
<td>Recupera un puntatore al primo carattere in un percorso che segue la lettera di unità o gli elementi del percorso di condivisione/server UNC.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a><br/></td>
<td>Rimuove la parte relativa al percorso di un percorso e di un file completi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a><br/></td>
<td>Rimuove tutti gli elementi di file e directory in un percorso, ad eccezione delle informazioni radice.<br/>
<blockquote>
[!Note]<br />
L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>la funzione PathCchStripToRoot</strong></a> più sicura.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br/></td>
<td>Rimuove l'elemento decorativo da una stringa di percorso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br/></td>
<td>Sostituisce determinati nomi di cartella in un percorso completo con la stringa di ambiente associata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br/></td>
<td>Rimuove gli attributi da una cartella che la rende una cartella di sistema. Questa cartella deve esistere effettivamente nel file system.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a><br/></td>
<td>Rimuove le virgolette dall'inizio e dalla fine di un percorso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br/></td>
<td>Controlla un contesto di associazione per verificare se è sicuro eseguire l'associazione a un particolare oggetto componente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br/></td>
<td>Determina uno schema per una stringa URL specificata e restituisce una stringa con un prefisso appropriato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br/></td>
<td>Converte una stringa dell'URL in forma canonica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br/></td>
<td>Se specificato con un URL relativo e la relativa base, restituisce un URL in formato canonico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br/></td>
<td>Esegue un confronto tra maiuscole e minuscole di due stringhe URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br/></td>
<td>Converte un percorso MS-DOS in un URL in formato canonico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br/></td>
<td>Converte i caratteri o le coppie di surrogati in un URL che potrebbero essere modificati durante il trasporto su Internet (caratteri non sicuri) nelle sequenze di &quot; &quot; escape corrispondenti. Le coppie di surrogati sono caratteri compresi tra U+10000 e U+10FFFF (in UTF-32) o tra DC00 e DFFF (in UTF-16). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br/></td>
<td>Macro che converte gli spazi nella sequenza di escape corrispondente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br/></td>
<td>Recupera il percorso da un URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br/></td>
<td>Accetta una stringa URL e restituisce una parte specificata di tale URL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br/></td>
<td>Esegue l'hashing di una stringa URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>URLIs</strong></a><br/></td>
<td>Verifica se un URL è un tipo specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br/></td>
<td>Verifica un URL per determinare se si tratta di un URL di file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br/></td>
<td>Restituisce un valore che indica se un URL è un URL che i browser in genere non includono nella cronologia di navigazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br/></td>
<td>Restituisce un valore che indica se un URL è opaco.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br/></td>
<td>Converte di nuovo le sequenze di escape in caratteri normali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br/></td>
<td>Converte di nuovo le sequenze di escape in caratteri normali e sovrascrive la stringa originale.<br/></td>
</tr>
</tbody>
</table>



 

 

 





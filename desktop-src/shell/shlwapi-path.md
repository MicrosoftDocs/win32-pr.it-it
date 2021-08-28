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
ms.openlocfilehash: 90937e4aa3c93c14957ec0db7f081c1cb598989e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481967"
---
# <a name="shell-path-handling-functions"></a>Funzioni di gestione del percorso della shell

In questa sezione vengono descritte le Windows di gestione dei percorsi della shell. Gli elementi di programmazione illustrati in questa documentazione vengono esportati Shlwapi.dll e definiti in Shlwapi.h e Shlwapi.lib.

## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a><br /> | Aggiunge una barra rovesciata alla fine di una stringa per creare la sintassi corretta per un percorso. Se il percorso di origine ha già una barra rovesciata finale, non verrà aggiunta alcuna barra rovesciata. <br /><blockquote>[!Note]<br />L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> più sicura.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a><br /> | Aggiunge un'estensione di file a una stringa di percorso.<br /><blockquote>[!Note]<br />L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>la funzione PathCchAddExtension</strong></a> più sicura.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a><br /> | Aggiunge un percorso alla fine di un altro. <br /><blockquote>[!Note]<br />L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> più sicura.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a><br /> | Crea un percorso radice da un numero di unità specificato.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a><br /> | Semplifica un percorso rimuovendo elementi di navigazione come "." e ".." per produrre un percorso diretto e ben formato.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a><br /> | Concatena due stringhe che rappresentano percorsi correttamente formati in un unico percorso. concatena anche tutti gli elementi del percorso relativo. <br /><blockquote>[!Note]<br />L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare al suo posto la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> più sicura.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a><br /> | Confronta due percorsi per determinare se condividono un prefisso comune. Un prefisso è uno dei tipi seguenti: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a><br /> | Tronca un percorso di file in base a una larghezza in pixel specificata sostituendo i componenti del percorso con puntini di sospensione.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a><br /> | Tronca un tracciato per rientrare in un determinato numero di caratteri sostituendo i componenti del tracciato con puntini di sospensione.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br /> | Converte l'URL di un file in un percorso Microsoft MS-DOS.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br /> | Crea un percorso da un URL di file.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a><br /> | Determina se un percorso di un file system, ad esempio un file o una cartella, è valido.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a><br /> | Cerca un'estensione in un percorso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a><br /> | Cerca un nome file in un percorso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br /> | Analizza un percorso e restituisce la parte di tale percorso che segue la prima barra rovesciata.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br /> | Cerca un file.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br /> | Determina se un nome di file specificato ha uno di un elenco di suffissi.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br /> | Trova gli argomenti della riga di comando all'interno di un percorso specificato.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br /> | Determina il tipo di carattere in relazione a un percorso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a><br /> | Cerca in un percorso una lettera di unità nell'intervallo da "A" a "Z" e restituisce il numero di unità corrispondente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br /> | Determina se il tipo di contenuto registrato di un file corrisponde al tipo di contenuto specificato. Questa funzione ottiene il tipo di contenuto per il tipo di file specificato e confronta tale stringa con <em>pszContentType</em>. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a><br /> | Verifica che un percorso sia una directory valida.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br /> | Determina se un percorso specificato è una directory vuota.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br /> | Cerca in un percorso tutti i caratteri di delimitazione del percorso ,ad esempio ':' o \' '. Se non sono presenti caratteri di delimitazione del percorso, il percorso viene considerato un percorso di specifica file.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br /> | Determina se un file è un file HTML. La determinazione viene effettuata in base al tipo di contenuto registrato per l'estensione del file.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br /> | Determina se un nome file è in formato lungo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br /> | Determina se una stringa di percorso rappresenta una risorsa di rete.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a><br /> | Cerca in un percorso per determinare se contiene un prefisso valido del tipo passato da <em>pszPrefix</em>. Un prefisso è uno dei tipi seguenti: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a><br /> | Cerca un percorso e determina se è relativo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a><br /> | Determina se una stringa di percorso fa riferimento alla radice di un volume.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a><br /> | Confronta due percorsi per determinare se hanno un componente radice comune.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br /> | Determina se una cartella esistente contiene gli attributi che la rendono una cartella di sistema. In alternativa, questa funzione indica se determinati attributi qualificano una cartella come cartella di sistema.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a><br /> | Determina se una stringa di percorso è un percorso Universal Naming Convention (UNC) valido, anziché un percorso basato su una lettera di unità.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a><br /> | Determina se una stringa è un UNC valido solo per un percorso del server.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a><br /> | Determina se una stringa è un percorso di condivisione UNC valido, \\ <em>condivisione server</em> \<em> </em> .<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br /> | Verifica una determinata stringa per determinare se è conforme a un formato URL valido.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br /> | Converte un percorso tutto maiuscolo in tutti i caratteri minuscoli per assegnare al percorso un aspetto coerente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br /> | Assegna a una cartella esistente gli attributi adeguati per diventare una cartella di sistema.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br /> | Cerca una stringa usando un tipo di corrispondenza con caratteri jolly MS-DOS.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br /> | Corrisponde a un nome di file da un percorso rispetto a uno o più modelli di nome file.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br /> | Analizza una stringa di percorso del file che contiene un percorso di file e un indice di icona e restituisce valori separati.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br /> | Cerca spazi in un percorso. Se vengono trovati spazi, l'intero percorso è racchiuso tra virgolette.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a><br /> | Crea un percorso relativo da un file o una cartella a un altro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a><br /> | Rimuove tutti gli argomenti da un percorso specificato.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a><br /> | Rimuove la barra rovesciata finale da un percorso specificato.<br /><blockquote>[!Note]<br />Questa funzione è deprecata. È consigliabile usare la <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>funzione PathCchRemoveBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> al suo posto.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a><br /> | Rimuove tutti gli spazi iniziali e finali da una stringa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a><br /> | Rimuove l'estensione di file da un percorso, se presente. <br /><blockquote>[!Note]<br />Questa funzione è deprecata. È consigliabile usare <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> al suo posto.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a><br /> | Rimuove il nome del file finale e la barra rovesciata da un percorso, se presenti.<br /><blockquote>[!Note]<br />Questa funzione è deprecata. È consigliabile usare la <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>funzione PathCchRemoveFileSpec</strong></a> al suo posto.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br /> | Sostituisce l'estensione di un nome file con una nuova estensione. Se il nome file non contiene un'estensione, l'estensione verrà collegata alla fine della stringa.<br /><blockquote>[!Note]<br />L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> più sicura al suo posto.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br /> | Determina se un percorso specificato è formattato correttamente e completo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br /> | Imposta il testo di un controllo figlio in una finestra o in una finestra di dialogo usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> per assicurarsi che il percorso si adatti al controllo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a><br /> | Recupera un puntatore al primo carattere in un percorso che segue la lettera di unità o gli elementi del percorso di condivisione/server UNC.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a><br /> | Rimuove la parte relativa al percorso di un percorso completo e di un file.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a><br /> | Rimuove tutti gli elementi di file e directory in un percorso ad eccezione delle informazioni radice.<br /><blockquote>[!Note]<br />L'uso improprio di questa funzione può causare un sovraccarico del buffer. È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> più sicura al suo posto.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br /> | Rimuove la decorazione da una stringa di percorso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br /> | Sostituisce determinati nomi di cartella in un percorso completo con la stringa di ambiente associata.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br /> | Rimuove gli attributi da una cartella che lo rende una cartella di sistema. Questa cartella deve esistere effettivamente nel file system.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a><br /> | Rimuove le virgolette dall'inizio e dalla fine di un percorso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>ShSkipJunction</strong></a><br /> | Controlla un contesto di associazione per verificare se è sicuro eseguire l'associazione a un determinato oggetto componente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br /> | Determina uno schema per una stringa URL specificata e restituisce una stringa con un prefisso appropriato.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br /> | Converte una stringa dell'URL in forma canonica.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br /> | Se viene fornito con un URL relativo e la relativa base, restituisce un URL in formato canonico.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br /> | Esegue un confronto tra maiuscole e minuscole di due stringhe URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br /> | Converte un percorso MS-DOS in un URL canonico.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br /> | Converte i caratteri o le coppie di surrogati in un URL che potrebbero essere modificati durante il trasporto su Internet ("caratteri non sicuri") nelle sequenze di escape corrispondenti. Le coppie di surrogati sono caratteri compresi tra U+10000 e U+10FFFF (in UTF-32) o tra DC00 e DFFF (in UTF-16). <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br /> | Macro che converte gli spazi nella sequenza di escape corrispondente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br /> | Recupera il percorso da un URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br /> | Accetta una stringa URL e restituisce una parte specificata di tale URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br /> | Esegue l'hashing di una stringa URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>URLI</strong></a><br /> | Verifica se un URL è un tipo specificato.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br /> | Verifica un URL per determinare se si tratta di un URL di file.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br /> | Restituisce un valore che indica se un URL è un URL che i browser in genere non includono nella cronologia di navigazione.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br /> | Restituisce un valore che indica se un URL è opaco.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br /> | Converte le sequenze di escape in caratteri normali.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br /> | Converte le sequenze di escape in caratteri normali e sovrascrive la stringa originale.<br /> | 




 

 

 





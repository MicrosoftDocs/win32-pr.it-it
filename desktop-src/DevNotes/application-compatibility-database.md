---
description: L'infrastruttura di compatibilità usa un database per identificare i problemi di compatibilità delle applicazioni e le relative soluzioni.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Database di compatibilità delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747967"
---
# <a name="application-compatibility-database"></a>Database di compatibilità delle applicazioni

L'infrastruttura di compatibilità usa un database per identificare i problemi di compatibilità delle applicazioni e le relative soluzioni. Questo database è un file binario indicizzato con estensione sdb. L'infrastruttura di compatibilità fornisce un'interfaccia di programmazione per accedere al database.

I problemi di compatibilità possono essere risolti in base alle singole applicazioni in fase di esecuzione. Ogni applicazione specificata nel database contiene uno o più componenti che necessitano di una soluzione. I componenti sono file eseguibili che vengono in genere descritti utilizzando i rispettivi attributi di file, ad esempio checksum.

Il processo di ricerca del database e di determinazione delle soluzioni per ogni applicazione viene chiamato *corrispondente*. Per creare una corrispondenza univoca, è possibile usare gli attributi di file e la presenza di file associati nella cartella o nella sottocartella che contiene il file con estensione exe. I file associati sono denominati *file corrispondenti*.

Un *tag* è un identificatore univoco per le voci e gli attributi nel database. Il *tipo di tag* indica il formato dei dati associati al [**tag**](tag.md). Ad esempio, **il \_ nome del tag** è di tipo **tag \_ \_ STRINGREF**. i dati per il **\_ nome del tag** sono una stringa del nome. Un *TagId* è un puntatore a una voce in un particolare database. Un *TAGREF* è un puntatore a una voce che può essere utilizzata in più database.

*Gli attributi di file* sono metadati associati a un file su disco. Questi attributi includono il nome file, le dimensioni del file, il checksum, la versione e la data. Questi attributi vengono utilizzati per determinare se un file caricato dal sistema corrisponde a una voce di database. Pertanto, questi attributi di file sono denominati anche *attributi corrispondenti*.

## <a name="solutions"></a>Soluzioni

Le soluzioni più comuni applicate ai componenti di un'applicazione sono AppHelp e AppFix.

Con AppHelp, viene visualizzata una notifica di messaggio localizzata personalizzata, in genere quando l'applicazione viene installata o avviata. Contiene un breve testo che illustra il problema di compatibilità e fornisce la possibilità di continuare a eseguire l'applicazione. Tuttavia, alcune applicazioni avranno esito negativo in modo significativo. Apphelp non fornirà all'utente la possibilità di continuare a eseguire queste applicazioni.

Con AppFix, vengono installati hook per le API chiamate dai componenti dell'applicazione. Questi hook puntano alle funzioni stub che possono essere chiamate al posto delle funzioni di sistema (note anche come *spessoramento*). Le funzioni Stub eseguono le operazioni necessarie per consentire l'esecuzione dell'applicazione nella versione installata di Windows. Ogni funzione stub può chiamare facoltativamente la funzione di sistema dopo aver completato il lavoro. Un *livello* o una *modalità* di compatibilità contiene uno o più shim e flag.

## <a name="in-this-section"></a>Contenuto della sezione

-   [**\_dati APPHELP**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**TROVA \_ informazioni**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**tipo di percorso \_**](path-type.md)
-   [**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
-   [**SdbCloseDatabase**](sdbclosedatabase.md)
-   [**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
-   [**SdbCommitIndexes**](sdbcommitindexes.md)
-   [**SdbCreateDatabase**](sdbcreatedatabase.md)
-   [**SdbDeclareIndex**](sdbdeclareindex.md)
-   [**SdbEndWriteListTag**](sdbendwritelisttag.md)
-   [**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
-   [**SdbFindFirstTag**](sdbfindfirsttag.md)
-   [**SdbFindNextTag**](sdbfindnexttag.md)
-   [**SdbFormatAttribute**](sdbformatattribute.md)
-   [**SdbFreeFileAttributes**](sdbfreefileattributes.md)
-   [**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
-   [**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
-   [**SdbGetFileAttributes**](sdbgetfileattributes.md)
-   [**SdbGetFirstChild**](sdbgetfirstchild.md)
-   [**SdbGetIndex**](sdbgetindex.md)
-   [**SdbGetMatchingExe**](sdbgetmatchingexe.md)
-   [**SdbGetNextChild**](sdbgetnextchild.md)
-   [**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
-   [**SdbGetTagFromTagID**](sdbgettagfromtagid.md)
-   [**SdbInitDatabase**](sdbinitdatabase.md)
-   [**SdbIsStandardDatabase**](sdbisstandarddatabase.md)
-   [**SdbMakeIndexKeyFromString**](sdbmakeindexkeyfromstring.md)
-   [**SdbOpenApphelpDetailsDatabase**](sdbopenapphelpdetailsdatabase.md)
-   [**SdbOpenApphelpResourceFile**](sdbopenapphelpresourcefile.md)
-   [**SdbOpenDatabase**](sdbopendatabase.md)
-   [**SdbQueryDataExTagID**](sdbquerydataextagid.md)
-   [**SDBQUERYRESULT**](sdbqueryresult.md)
-   [**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
-   [**SdbReadBinaryTag**](sdbreadbinarytag.md)
-   [**SdbReadDWORDTag**](sdbreaddwordtag.md)
-   [**SdbReadQWORDTag**](sdbreadqwordtag.md)
-   [**SdbReadStringTag**](sdbreadstringtag.md)
-   [**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
-   [**SdbReleaseDatabase**](sdbreleasedatabase.md)
-   [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
-   [**SdbStartIndexing**](sdbstartindexing.md)
-   [**SdbStopIndexing**](sdbstopindexing.md)
-   [**SdbTagRefToTagID**](sdbtagreftotagid.md)
-   [**SdbTagToString**](sdbtagtostring.md)
-   [**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
-   [**SdbWriteBinaryTag**](sdbwritebinarytag.md)
-   [**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
-   [**SdbWriteDWORDTag**](sdbwritedwordtag.md)
-   [**SdbWriteNULLTag**](sdbwritenulltag.md)
-   [**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
-   [**SdbWriteStringTag**](sdbwritestringtag.md)
-   [**SdbWriteWORDTag**](sdbwritewordtag.md)
-   [**Tipi di database shim**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**TAG**](tag.md)
-   [**Tipi di TAG**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 




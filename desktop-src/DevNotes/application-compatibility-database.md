---
description: L'infrastruttura di compatibilità usa un database per identificare i problemi di compatibilità delle applicazioni e le relative soluzioni.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Database di compatibilità delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787e8dbc9aa07bc8d466dae766c3fed406692dbd32e128123c4b37d9a7a5618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956160"
---
# <a name="application-compatibility-database"></a>Database di compatibilità delle applicazioni

L'infrastruttura di compatibilità usa un database per identificare i problemi di compatibilità delle applicazioni e le relative soluzioni. Questo database è un file binario indicizzato con estensione sdb. L'infrastruttura di compatibilità fornisce un'interfaccia di programmazione per accedere al database.

I problemi di compatibilità possono essere risolti in base all'applicazione in fase di esecuzione. Ogni applicazione specificata nel database contiene uno o più componenti che necessitano di una soluzione. I componenti sono file eseguibili descritti in genere usando i relativi attributi di file, ad esempio il checksum.

Il processo di ricerca del database e di determinazione delle soluzioni per ogni applicazione è detto *corrispondenza.* Gli attributi di file e la presenza di file associati nella cartella o sottocartella che contiene .exe file possono essere usati per creare una corrispondenza univoca. I file associati sono denominati *file corrispondenti.*

UN *TAG* è un identificatore univoco per le voci e gli attributi nel database. Il *tipo TAG* indica il formato dei dati associati a [**TAG**](tag.md). Ad esempio, **TAG \_ NAME** è di tipo **TAG TYPE \_ \_ STRINGREF;** i dati per **TAG \_ NAME** sono una stringa di nome. Un *TAGID* è un puntatore a una voce in un database specifico. UN *TAGREF* è un puntatore a una voce che può essere usata in più database.

*Gli attributi* di file sono metadati associati a un file su disco. Questi attributi includono il nome del file, le dimensioni del file, il checksum, la versione e la data. Questi attributi vengono usati per determinare se un file caricato dal sistema corrisponde a una voce di database. Di conseguenza, questi attributi di file vengono chiamati anche *attributi corrispondenti.*

## <a name="solutions"></a>Soluzioni

Le soluzioni più comuni applicate ai componenti di un'applicazione sono Apphelp e Appfix.

Con Apphelp viene visualizzata una notifica personalizzata dei messaggi localizzati, in genere quando l'applicazione viene installata o avviata. Contiene un breve testo che illustra il problema di compatibilità e offre la possibilità di continuare a eseguire l'applicazione. Tuttavia, l'esecuzione di alcune applicazioni avrà un notevole esito negativo. Apphelp non offrirà all'utente la possibilità di continuare a eseguire queste applicazioni.

Con Appfix, gli hook vengono installati per le API chiamate dai componenti dell'applicazione. Questi hook puntano a funzioni stub che possono essere chiamate al posto delle funzioni di sistema (note anche *come shimming*). Le funzioni stub eseguono le operazioni necessarie per consentire l'esecuzione dell'applicazione nella versione installata di Windows. Ogni funzione stub può facoltativamente chiamare la funzione di sistema dopo aver completato il proprio lavoro. Un *livello di compatibilità* *o una modalità* contiene uno o più s shims e flag.

## <a name="in-this-section"></a>Contenuto della sezione

-   [**DATI DI \_ APPHELP**](apphelp-data.md)
-   [**Attrinfo**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**INFORMAZIONI DI \_ RICERCA**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**TIPO \_ DI PERCORSO**](path-type.md)
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
-   [**Tipi di database Shim**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**TAG**](tag.md)
-   [**Tipi TAG**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 




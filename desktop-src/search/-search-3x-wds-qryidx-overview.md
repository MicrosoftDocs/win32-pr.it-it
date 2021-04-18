---
description: Sono disponibili diversi modi per utilizzare la ricerca di Windows per eseguire una query sull'indice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Esecuzione di query sull'indice a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306176"
---
# <a name="querying-the-index-programmatically"></a>Esecuzione di query sull'indice a livello di codice

Sono disponibili diversi modi per utilizzare la ricerca di Windows per eseguire una query sull'indice.

Questa sezione fornisce il framework concettuale per l'esecuzione di query sull'indice a livello di codice:

-   [Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice](using-sql-and-aqs-to-query-the-index.md)
-   [Esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)
-   [Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows](-search-sql-windowssearch-entry.md)
-   [Uso della sintassi avanzata delle query a livello di codice](-search-3x-advancedquerysyntax.md)

> [!Note]  
> Compatibilità di Microsoft Windows Desktop Search (WDS) 2x: nei computer che eseguono Windows XP e versioni successive [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) è deprecato. Gli sviluppatori devono invece usare [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) per ottenere una stringa di connessione e analizzare la query dell'utente in Structured Query Language (SQL), quindi eseguire una query tramite il collegamento all'oggetto e il database di incorporamento (OLE DB).

 

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni su OLE DB, vedere [Cenni preliminari sulla programmazione OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx). Per informazioni sul provider di dati di .NET Framework per OLE DB, vedere lo [spazio dei nomi System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Per ulteriori informazioni sull'utilizzo delle proprietà nell'esecuzione di query, vedere gli argomenti seguenti:
    -   [Sistema di proprietà](../properties/building-property-handlers.md)
    -   [Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Per informazioni su come creare e modificare le cartelle di ricerca, vedere [**interfaccia ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   Per le bacheche dei messaggi di discussione e domande supportate dalla community sulle tecnologie di ricerca, vedere il [Forum MSDN relativo allo sviluppo per Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Per scaricare gli esempi di codice dell'SDK di ricerca:
    -   Per Windows 7: [esempi di Windows Search su GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   Per Windows Vista: [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   Per scaricare il Windows SDK:
    -   Per Windows 7: [Windows SDK per Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   Per Windows Vista: [Windows SDK per Windows Vista e .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida allo sviluppo di Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Estensione dell'indice di ricerca di Windows](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Estensione delle risorse della lingua](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 

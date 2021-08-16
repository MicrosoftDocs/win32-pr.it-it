---
description: Esistono diversi modi per usare Windows ricerca per eseguire query sull'indice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Esecuzione di query sull'indice a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76f98d12e4a0615bf19dfb165766a67b8c9e58700ad2d0c897782e2a16ba9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094942"
---
# <a name="querying-the-index-programmatically"></a>Esecuzione di query sull'indice a livello di codice

Esistono diversi modi per usare Windows ricerca per eseguire query sull'indice.

Questa sezione illustra il framework concettuale per l'esecuzione di query sull'indice a livello di codice:

-   [Uso SQL e approcci AQS per eseguire query sull'indice](using-sql-and-aqs-to-query-the-index.md)
-   [Esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)
-   [Esecuzione di query sull'indice con Windows sintassi SQL ricerca](-search-sql-windowssearch-entry.md)
-   [Uso della sintassi di query avanzata a livello di codice](-search-3x-advancedquerysyntax.md)

> [!Note]  
> Compatibilità 2x di Microsoft Windows Desktop Search (WDS) legacy: nei computer che eseguono Windows XP e versioni successive, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) è deprecato. Gli sviluppatori devono invece usare [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) per ottenere una stringa di connessione e analizzare la query dell'utente in Structured Query Language (SQL) e quindi eseguire una query tramite Object Linking and Embedding Database (OLE DB).

 

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sui OLE DB, vedere OLE DB [Programming Overview](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx). Per informazioni sul .NET Framework provider di dati per OLE DB, vedere lo spazio dei nomi [System.Data.OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Per altre informazioni sull'uso delle proprietà nell'esecuzione di query, vedere gli argomenti seguenti:
    -   [Sistema di proprietà](../properties/building-property-handlers.md)
    -   [Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Per informazioni su come creare e modificare le cartelle di ricerca, vedere [**Interfaccia ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   Per le bacheche per domande e discussioni supportate dalla community sulle tecnologie di ricerca, vedere [forum MSDN: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Per scaricare gli esempi di codice dell'SDK di ricerca:
    -   Per Windows 7: [Windows esempi di ricerca in GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   Per Windows Vista: esempi [Windows SDK di ricerca](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   Per scaricare Windows SDK:
    -   Per Windows 7: [Windows SDK per Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   Per Windows Vista: [Windows SDK per Windows Vista e .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Guida allo sviluppo della ricerca](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Estensione dell'Windows di ricerca](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Estensione delle risorse del linguaggio](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 

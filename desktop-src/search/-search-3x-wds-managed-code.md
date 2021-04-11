---
description: Windows Search SDK fornisce un assembly di interoperabilità che consente di utilizzare gli oggetti Component Object Model (COM) esposti da ricerca di Windows e altri programmi rispetto alle interfacce e alle classi utilizzando codice gestito.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Uso di codice gestito con i dati della shell e Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128607"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Uso di codice gestito con i dati della shell e Windows Search

Windows Search SDK fornisce un assembly di interoperabilità che consente di utilizzare gli oggetti Component Object Model (COM) esposti da ricerca di Windows e altri programmi rispetto alle interfacce e alle classi utilizzando codice gestito. L'assembly di interoperabilità è firmato digitalmente da Microsoft e può essere trovato con gli [esempi di Windows Search](-search-samples-ovw.md).

Questo argomento è organizzato nel modo seguente:

-   [Uso del codepack API Windows](#using-the-windows-api-codepack)
    -   [Accesso ai risultati dell'indice](#accessing-index-results)
    -   [Applicazione di esempio con il codepack API Windows](#sample-application-using-the-windows-api-codepack)
-   [Argomenti correlati](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Uso del codepack API Windows

Se si lavora nell'ambiente Microsoft .NET, usare il pacchetto di [codice dell'API Windows per Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) per ottenere i risultati della ricerca o semplicemente esplorare lo spazio dei nomi. Il [pacchetto di codice API Windows per Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) fornisce una raccolta di elementi della shell che sono essenzialmente wrapper intorno all' [interfaccia IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)nativa. È possibile eseguire l'iterazione di questa raccolta e ottenere i diversi valori di proprietà in modo analogo a come si enumerano i risultati in una tabella da una query di collegamento e incorporamento di un database (OLE DB).

Il frammento di codice seguente illustra come eseguire l'iterazione degli elementi di ricerca e ottenere i valori delle proprietà per ognuno.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Accesso ai risultati dell'indice

È possibile accedere ai risultati degli indici tramite OLE DB o il modello di dati della shell. Uno dei due approcci presenta vantaggi e svantaggi. Un vantaggio è che OLE DB e Structured Query Language (SQL) sono familiari ai programmatori di database. Altri vantaggi sono il controllo migliore sulle prestazioni quando si eseguono query solo nell'indicizzatore e l'accesso a funzionalità aggiuntive, ad esempio la possibilità di individuare rapidamente i risultati precedenti in un nuovo set di righe.

I vantaggi del modello di dati della shell sono l'astrazione tra diverse fonti di informazioni, ad esempio OpenSearch, e fornisce l'accesso a funzionalità aggiuntive, ad esempio anteprime e gestori di proprietà. Il modello a oggetti della shell, inoltre, richiede un supporto speciale per i risultati non filename, ad esempio gli elementi di posta e i risultati di OneNote, né per gli elementi che si trovano nell'indice dell'utente. Si noti che nella shell [KNOWNFOLDERID](../shell/knownfolderid.md) è l'ambito di cartella noto per il contenuto indicizzato locale. Per ulteriori informazioni sulla creazione di un'origine dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Le origini dati OpenSearch non vengono esposte tramite OLE DB per la ricerca federata in Windows 7 e versioni successive. Per questo motivo, è consigliabile prendere in considerazione la scrittura di un provider LINQ per lo spazio dei nomi della shell invece di usare OLE DB per accedere ai risultati dell'indicizzatore. Per ulteriori informazioni, vedere [procedura dettagliata: creazione di un provider LINQ IQueryable](/previous-versions/bb546158(v=vs.140)).

### <a name="sample-application-using-the-windows-api-codepack"></a>Applicazione di esempio con il codepack API Windows

Lo screenshot seguente rappresenta una simulazione di un'applicazione di esempio creata con il [pacchetto di codice API Windows per Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).

![screenshot dell'applicazione Media Player che mostra i messaggi di posta elettronica](images/folderid-searchhome.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Interoperabilità tra linguaggi diversi](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 

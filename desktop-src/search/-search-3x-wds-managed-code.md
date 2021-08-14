---
description: L'SDK di Windows Search fornisce un assembly di interoperabilità che consente di usare oggetti Component Object Model (COM) esposti da ricerca di Windows e altri programmi su interfacce e classi che usano codice gestito.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Uso di codice gestito con i dati della shell e Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26276236c2dee056f603d359a89560e9b1ce9e06b0b3f1cfed2c68f77b0b0eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052244"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Uso di codice gestito con i dati della shell e Windows Search

L'SDK di Windows Search fornisce un assembly di interoperabilità che consente di usare oggetti Component Object Model (COM) esposti da ricerca di Windows e altri programmi su interfacce e classi che usano codice gestito. L'assembly di interoperabilità è firmato digitalmente da Microsoft ed è disponibile con gli esempi [Windows search](-search-samples-ovw.md).

Questo argomento è organizzato come segue:

-   [Uso dell'API Windows CodePack](#using-the-windows-api-codepack)
    -   [Accesso ai risultati dell'indice](#accessing-index-results)
    -   [Applicazione di esempio con codepack Windows'API di esempio](#sample-application-using-the-windows-api-codepack)
-   [Argomenti correlati](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Uso dell'API Windows CodePack

Se si lavora nell'ambiente Microsoft .NET, usare il code [pack dell'API Windows](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) per Microsoft .NET Framework per ottenere i risultati della ricerca o semplicemente esplorare lo spazio dei nomi . Il [Windows code pack dell'API](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) per Microsoft .NET Framework fornisce una raccolta di elementi della shell che sono essenzialmente wrapper per l'interfaccia [IShellItem nativa.](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem) È possibile scorrere questa raccolta e ottenere i vari valori delle proprietà in modo simile a come enumerare i risultati in una tabella da una query Object Linking and Embedding Database (OLE DB).

Il frammento di codice seguente illustra come scorrere gli elementi di ricerca e ottenere i valori delle proprietà per ognuno di essi.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Accesso ai risultati dell'indice

È possibile accedere ai risultati dell'indice OLE DB o il modello di dati shell. Entrambi gli approcci presentano vantaggi e svantaggi. Uno dei vantaggi è che OLE DB e Structured Query Language (SQL) hanno familiarità con i programmatori di database. Altri vantaggi sono un migliore controllo sulle prestazioni quando si esegue una query solo sull'indicizzatore e l'accesso a funzionalità aggiuntive, ad esempio la possibilità di individuare rapidamente i risultati precedenti in un nuovo set di righe.

I vantaggi del modello di dati shell sono l'astrazione tra diverse origini di informazioni, ad esempio OpenSearch, e l'accesso a funzionalità aggiuntive, ad esempio anteprime e gestori di proprietà. Né il modello a oggetti shell richiede un supporto caso speciale per i risultati non di nome file, ad esempio elementi di posta elettronica e risultati OneNote, né per qualsiasi elemento che risiede nell'indice dell'utente. Si noti che nella shell [KNOWNFOLDERID è](../shell/knownfolderid.md) l'ambito di cartella noto per il contenuto indicizzato locale. Per altre informazioni sulla creazione di un'origine dati shell, vedere [Implementazione delle interfacce dell'oggetto cartella di base.](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))

OpenSearch origini dati non vengono esposte tramite OLE DB per la ricerca federata in Windows 7 e versioni successive. Per questo motivo è consigliabile scrivere un provider LINQ per lo spazio dei nomi Shell anziché usare OLE DB per accedere ai risultati dell'indicizzatore. Per altre informazioni, vedere [Procedura dettagliata: Creazione di un provider LINQ IQueryable.](/previous-versions/bb546158(v=vs.140))

### <a name="sample-application-using-the-windows-api-codepack"></a>Applicazione di esempio con codepack Windows'API di esempio

Lo screenshot seguente rappresenta un mock up di un'applicazione di esempio creata con il [code pack dell'API Windows](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)per Microsoft .NET Framework .

![Screenshot dell'applicazione lettore multimediale che mostra i messaggi di posta elettronica](images/folderid-searchhome.png)

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

 

 

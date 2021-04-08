---
title: Chiamata di WDS a livello di codice
description: È possibile eseguire query a livello di programmazione in Microsoft Windows Desktop Search (WDS) 2. x usando i metodi ExecuteQuery e ExecuteSQLQuery nell'interfaccia ISearchDesktop.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727050"
---
# <a name="calling-wds-programmatically"></a>Chiamata di WDS a livello di codice

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

È possibile eseguire query a livello di programmazione in Microsoft Windows Desktop Search (WDS) 2. x usando i metodi **ExecuteQuery** e **ExecuteSQLQuery** nell'interfaccia [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) . Il metodo **ExecuteQuery** restituisce un set di record dall'indice basato sul testo della query, sulle colonne e sulle restrizioni passate come parametri. Il metodo **ExecuteSQLQuery** restituisce anche un set di record di risultati, ma richiede il passaggio esatto del Structured Query Language (SQL). **ExecuteQuery** deve essere usato nella maggior parte degli scenari.

## <a name="regular-queries"></a>Query normali

Le query regolari sono quelle digitate nella casella di input WDS dall'utente, inclusa la [sintassi di query avanzata](-search-2x-wds-aqsreference.md). La query viene passata a **ExecuteQuery** insieme alle colonne [dello schema](-search-2x-wds-schematable.md) WDS 2. x da restituire, alla colonna e all'ordine di ordinamento dei risultati e a qualsiasi clausola per limitare i risultati in base a.

Il metodo ha il formato seguente:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Direzione | Variabile           | Descrizione                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| In        | lpcwstrQuery       | Testo della query. Questa query è identica a quella di una query digitata nella casella di testo Cerca nell'interfaccia utente di ricerca desktop di Windows. <br/> ad esempio `"from:Zara dinner plans"`<br/> |
| In        | lpcwstrColumn      | Colonne da includere, separate da virgole. <br/> ad esempio `"DocTitle, Url"`<br/>                                                                                            |
| In        | lpcwstrSort        | Colonna di sostituzione in base alla quale eseguire l'ordinamento seguito da ASC per Ascending o DESC per la decrescente. <br/> ad esempio `"LastAuthor DESC"`<br/>                                                  |
| In        | lpcwstrRestriction | Restrizioni per accodare le clausole WHERE nella ricerca desktop di Windows Select. <br/> ad esempio `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| In uscita       | ppiRs              | Set di record risultante<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>Query SQL

Il **ISearchDesktop.Exemetodo cuteSQLQuery** viene usato per inviare query di database WDS dirette. La sintassi per le query è simile a quella usata per SharePoint Server, insieme alla possibilità di usare clausole GROUP BY di tipo Monarch. La query viene eseguita sull'indice esattamente come viene passata senza alcuna elaborazione aggiuntiva della sintassi avanzata delle query come l'API ExecuteQuery.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

Il metodo ha il formato seguente:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Direzione | Variabile   | Descrizione                                    |
|-----------|------------|------------------------------------------------|
| In        | lpcwstrSQL | Query SQL da eseguire sull'indice WDS |
| In uscita       | ppiRs      | Set di record risultante                       |



 

Risorse:

-   File di supporto per l'interfaccia ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip
-   Esempio di ISearchDesktop C#: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Codice C++ di esempio

> [!Note]
>
> QUESTO CODICE E LE INFORMAZIONI VENGONO FORNITE "COSÌ COME SONO" SENZA GARANZIA DI ALCUN TIPO, ESPRESSA O IMPLICITA, INCLUSE, A TITOLO ESEMPLIFICATIVO, LE GARANZIE IMPLICITE DI COMMERCIABILITÀ E/O IDONEITÀ PER UNO SCOPO SPECIFICO.
>
> Copyright (C) Microsoft. Tutti i diritti sono riservati.

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Sintassi di ricerca avanzata](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipi percepiti](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Chiamata di WDS da pagine Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 


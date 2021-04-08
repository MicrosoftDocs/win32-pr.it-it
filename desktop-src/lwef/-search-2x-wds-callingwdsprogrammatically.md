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
# <a name="calling-wds-programmatically"></a><span data-ttu-id="871c1-103">Chiamata di WDS a livello di codice</span><span class="sxs-lookup"><span data-stu-id="871c1-103">Calling WDS Programmatically</span></span>

> [!NOTE]
> <span data-ttu-id="871c1-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="871c1-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="871c1-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="871c1-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="871c1-106">È possibile eseguire query a livello di programmazione in Microsoft Windows Desktop Search (WDS) 2. x usando i metodi **ExecuteQuery** e **ExecuteSQLQuery** nell'interfaccia [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="871c1-106">Microsoft Windows Desktop Search (WDS) 2.x can be queried programmatically using the **ExecuteQuery** and **ExecuteSQLQuery** methods in the [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) interface.</span></span> <span data-ttu-id="871c1-107">Il metodo **ExecuteQuery** restituisce un set di record dall'indice basato sul testo della query, sulle colonne e sulle restrizioni passate come parametri.</span><span class="sxs-lookup"><span data-stu-id="871c1-107">The **ExecuteQuery** method returns a record set from the index based on the query text, columns, and restrictions passed as parameters.</span></span> <span data-ttu-id="871c1-108">Il metodo **ExecuteSQLQuery** restituisce anche un set di record di risultati, ma richiede il passaggio esatto del Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="871c1-108">The **ExecuteSQLQuery** method also returns a record set of results but requires the exact Structured Query Language (SQL) command to be passed in.</span></span> <span data-ttu-id="871c1-109">**ExecuteQuery** deve essere usato nella maggior parte degli scenari.</span><span class="sxs-lookup"><span data-stu-id="871c1-109">**ExecuteQuery** should be used in most scenarios.</span></span>

## <a name="regular-queries"></a><span data-ttu-id="871c1-110">Query normali</span><span class="sxs-lookup"><span data-stu-id="871c1-110">Regular Queries</span></span>

<span data-ttu-id="871c1-111">Le query regolari sono quelle digitate nella casella di input WDS dall'utente, inclusa la [sintassi di query avanzata](-search-2x-wds-aqsreference.md).</span><span class="sxs-lookup"><span data-stu-id="871c1-111">Regular queries are those typed into the WDS input box by the user including all [Advanced Query Syntax](-search-2x-wds-aqsreference.md).</span></span> <span data-ttu-id="871c1-112">La query viene passata a **ExecuteQuery** insieme alle colonne [dello schema](-search-2x-wds-schematable.md) WDS 2. x da restituire, alla colonna e all'ordine di ordinamento dei risultati e a qualsiasi clausola per limitare i risultati in base a.</span><span class="sxs-lookup"><span data-stu-id="871c1-112">The query is passed to **ExecuteQuery** along with the WDS 2.x [schema](-search-2x-wds-schematable.md) columns to return, the column and order to sort results, and any clauses to restrict results by.</span></span>

<span data-ttu-id="871c1-113">Il metodo ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="871c1-113">The method has the form:</span></span>

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| <span data-ttu-id="871c1-114">Direzione</span><span class="sxs-lookup"><span data-stu-id="871c1-114">Direction</span></span> | <span data-ttu-id="871c1-115">Variabile</span><span class="sxs-lookup"><span data-stu-id="871c1-115">Variable</span></span>           | <span data-ttu-id="871c1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="871c1-116">Description</span></span>                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="871c1-117">In</span><span class="sxs-lookup"><span data-stu-id="871c1-117">In</span></span>        | <span data-ttu-id="871c1-118">lpcwstrQuery</span><span class="sxs-lookup"><span data-stu-id="871c1-118">lpcwstrQuery</span></span>       | <span data-ttu-id="871c1-119">Testo della query.</span><span class="sxs-lookup"><span data-stu-id="871c1-119">The query text.</span></span> <span data-ttu-id="871c1-120">Questa query è identica a quella di una query digitata nella casella di testo Cerca nell'interfaccia utente di ricerca desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="871c1-120">This query is the same as a query typed into the search text box in the Windows Desktop Search user interface.</span></span> <br/> <span data-ttu-id="871c1-121">ad esempio `"from:Zara dinner plans"`</span><span class="sxs-lookup"><span data-stu-id="871c1-121">For example: `"from:Zara dinner plans"`</span></span><br/> |
| <span data-ttu-id="871c1-122">In</span><span class="sxs-lookup"><span data-stu-id="871c1-122">In</span></span>        | <span data-ttu-id="871c1-123">lpcwstrColumn</span><span class="sxs-lookup"><span data-stu-id="871c1-123">lpcwstrColumn</span></span>      | <span data-ttu-id="871c1-124">Colonne da includere, separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="871c1-124">The columns to include, separated by commas.</span></span> <br/> <span data-ttu-id="871c1-125">ad esempio `"DocTitle, Url"`</span><span class="sxs-lookup"><span data-stu-id="871c1-125">For example: `"DocTitle, Url"`</span></span><br/>                                                                                            |
| <span data-ttu-id="871c1-126">In</span><span class="sxs-lookup"><span data-stu-id="871c1-126">In</span></span>        | <span data-ttu-id="871c1-127">lpcwstrSort</span><span class="sxs-lookup"><span data-stu-id="871c1-127">lpcwstrSort</span></span>        | <span data-ttu-id="871c1-128">Colonna di sostituzione in base alla quale eseguire l'ordinamento seguito da ASC per Ascending o DESC per la decrescente.</span><span class="sxs-lookup"><span data-stu-id="871c1-128">The Override Column to sort by followed by ASC for ascending or DESC for descending.</span></span> <br/> <span data-ttu-id="871c1-129">ad esempio `"LastAuthor DESC"`</span><span class="sxs-lookup"><span data-stu-id="871c1-129">For example: `"LastAuthor DESC"`</span></span><br/>                                                  |
| <span data-ttu-id="871c1-130">In</span><span class="sxs-lookup"><span data-stu-id="871c1-130">In</span></span>        | <span data-ttu-id="871c1-131">lpcwstrRestriction</span><span class="sxs-lookup"><span data-stu-id="871c1-131">lpcwstrRestriction</span></span> | <span data-ttu-id="871c1-132">Restrizioni per accodare le clausole WHERE nella ricerca desktop di Windows Select.</span><span class="sxs-lookup"><span data-stu-id="871c1-132">Restrictions to append through WHERE clauses in the Windows Desktop Search select.</span></span> <br/> <span data-ttu-id="871c1-133">ad esempio `"Contains(LastAuthor, 'Bill')"`</span><span class="sxs-lookup"><span data-stu-id="871c1-133">For example: `"Contains(LastAuthor, 'Bill')"`</span></span><br/>                                       |
| <span data-ttu-id="871c1-134">In uscita</span><span class="sxs-lookup"><span data-stu-id="871c1-134">Out</span></span>       | <span data-ttu-id="871c1-135">ppiRs</span><span class="sxs-lookup"><span data-stu-id="871c1-135">ppiRs</span></span>              | <span data-ttu-id="871c1-136">Set di record risultante</span><span class="sxs-lookup"><span data-stu-id="871c1-136">The resulting record set</span></span><br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a><span data-ttu-id="871c1-137">Query SQL</span><span class="sxs-lookup"><span data-stu-id="871c1-137">SQL Queries</span></span>

<span data-ttu-id="871c1-138">Il **ISearchDesktop.Exemetodo cuteSQLQuery** viene usato per inviare query di database WDS dirette.</span><span class="sxs-lookup"><span data-stu-id="871c1-138">The **ISearchDesktop.ExecuteSQLQuery** method is used to send direct WDS database queries.</span></span> <span data-ttu-id="871c1-139">La sintassi per le query è simile a quella usata per SharePoint Server, insieme alla possibilità di usare clausole GROUP BY di tipo Monarch.</span><span class="sxs-lookup"><span data-stu-id="871c1-139">The syntax for the queries is similar to that used for SharePoint Server, along with the ability to use Monarch-style SQL GROUP BY clauses.</span></span> <span data-ttu-id="871c1-140">La query viene eseguita sull'indice esattamente come viene passata senza alcuna elaborazione aggiuntiva della sintassi avanzata delle query come l'API ExecuteQuery.</span><span class="sxs-lookup"><span data-stu-id="871c1-140">The query is executed against the index exactly as it is passed in with no additional processing of Advanced Query Syntax as the ExecuteQuery API does.</span></span>

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

<span data-ttu-id="871c1-141">Il metodo ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="871c1-141">The method has the form:</span></span>

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| <span data-ttu-id="871c1-142">Direzione</span><span class="sxs-lookup"><span data-stu-id="871c1-142">Direction</span></span> | <span data-ttu-id="871c1-143">Variabile</span><span class="sxs-lookup"><span data-stu-id="871c1-143">Variable</span></span>   | <span data-ttu-id="871c1-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="871c1-144">Description</span></span>                                    |
|-----------|------------|------------------------------------------------|
| <span data-ttu-id="871c1-145">In</span><span class="sxs-lookup"><span data-stu-id="871c1-145">In</span></span>        | <span data-ttu-id="871c1-146">lpcwstrSQL</span><span class="sxs-lookup"><span data-stu-id="871c1-146">lpcwstrSQL</span></span> | <span data-ttu-id="871c1-147">Query SQL da eseguire sull'indice WDS</span><span class="sxs-lookup"><span data-stu-id="871c1-147">The SQL query to execute against the WDS index</span></span> |
| <span data-ttu-id="871c1-148">In uscita</span><span class="sxs-lookup"><span data-stu-id="871c1-148">Out</span></span>       | <span data-ttu-id="871c1-149">ppiRs</span><span class="sxs-lookup"><span data-stu-id="871c1-149">ppiRs</span></span>      | <span data-ttu-id="871c1-150">Set di record risultante</span><span class="sxs-lookup"><span data-stu-id="871c1-150">The resulting record set</span></span>                       |



 

<span data-ttu-id="871c1-151">Risorse:</span><span class="sxs-lookup"><span data-stu-id="871c1-151">Resources:</span></span>

-   <span data-ttu-id="871c1-152">File di supporto per l'interfaccia ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip</span><span class="sxs-lookup"><span data-stu-id="871c1-152">Support files for the ISearchDesktop interface: https://addins.msn.com/support/WDSSDK.zip</span></span>
-   <span data-ttu-id="871c1-153">Esempio di ISearchDesktop C#: https://addins.msn.com/support/WDSSample.zip</span><span class="sxs-lookup"><span data-stu-id="871c1-153">ISearchDesktop C# Sample: https://addins.msn.com/support/WDSSample.zip</span></span>

## <a name="sample-c-code"></a><span data-ttu-id="871c1-154">Codice C++ di esempio</span><span class="sxs-lookup"><span data-stu-id="871c1-154">Sample C++ Code</span></span>

> [!Note]
>
> <span data-ttu-id="871c1-155">QUESTO CODICE E LE INFORMAZIONI VENGONO FORNITE "COSÌ COME SONO" SENZA GARANZIA DI ALCUN TIPO, ESPRESSA O IMPLICITA, INCLUSE, A TITOLO ESEMPLIFICATIVO, LE GARANZIE IMPLICITE DI COMMERCIABILITÀ E/O IDONEITÀ PER UNO SCOPO SPECIFICO.</span><span class="sxs-lookup"><span data-stu-id="871c1-155">THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.</span></span>
>
> <span data-ttu-id="871c1-156">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="871c1-156">Copyright (C) Microsoft.</span></span> <span data-ttu-id="871c1-157">Tutti i diritti sono riservati.</span><span class="sxs-lookup"><span data-stu-id="871c1-157">All rights reserved.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="871c1-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="871c1-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="871c1-159">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="871c1-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="871c1-160">Sintassi di ricerca avanzata</span><span class="sxs-lookup"><span data-stu-id="871c1-160">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="871c1-161">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="871c1-161">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="871c1-162">Chiamata di WDS da pagine Web</span><span class="sxs-lookup"><span data-stu-id="871c1-162">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 


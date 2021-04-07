---
title: Chiamata di WDS dalla riga di comando
description: È possibile avviare l'interfaccia utente di ricerca desktop Microsoft Windows con un filtro, un archivio e una query specifici da un'altra applicazione o da una pagina Web che usa l'oggetto browser helper (BHO) usando la sintassi della riga di comando windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724020"
---
# <a name="calling-wds-from-the-command-line"></a>Chiamata di WDS dalla riga di comando

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

È possibile avviare l'interfaccia utente di ricerca desktop Microsoft Windows con un filtro, un archivio e una query specifici da un'altra applicazione o da una pagina Web che usa l'oggetto browser helper (BHO) usando la sintassi della riga di comando windowssearch.exe. Quando si chiama WDS dalla riga di comando, non vengono restituite informazioni sulle azioni dell'utente o sulla selezione nella finestra WDS nell'applicazione chiamante o nella pagina Web.

Il percorso di installazione di WDS è specificato nell'impostazione del registro di sistema InstallDir in HKEY_LOCAL_MACHINE \\ software \\ Microsoft \\ Windows Desktop Search. Il percorso predefinito in cui è installato windowssearch.exe è file di programma \\ Windows Desktop Search.

## <a name="command-line-syntax"></a>Sintassi della riga di comando

La sintassi seguente si applica all'interfaccia della riga di comando di Windows Desktop Search 2. x.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzioni</th>
<th>Parametro</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/Startup</td>

<td>Inizializza la ricerca desktop di Windows</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Disattiva l'indicizzazione e ripete l'analisi di tutte le posizioni degli indici</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Mostra la finestra stato indicizzazione</td>
</tr>
<tr class="even">
<td>/launchsearchwindow o/URL</td>

<td>Apre una finestra di WDS con una query vuota</td>
</tr>
<tr class="odd">
<td>/URL</td>
<td>ricerca: [Store | Show | query] stringa di query</td>
<td>Apre una finestra di WDS con una query e un filtro in base ai parametri seguenti:
<ul>
<li><p>Store: specifica l'origine dati su cui eseguire la query: files, Outlook e outlookexpress. Se non viene specificato, verranno cercati tutti gli archivi. <br/></p>
<blockquote>
[!Note]<br />
Sebbene la sintassi di query avanzata supporti il riferimento a Microsoft Outlook come ' oe ', il parametro Store nella riga di comando deve essere ' outlookexpress '.
</blockquote>
<p><br/></p></li>
<li><p>Show-specifica il tipo di risultati percepito da restituire. Vedere <a href="-search-2x-wds-perceivedtype.md">tipi percepiti</a> per un elenco completo di tipi. Se non specificato, verranno restituiti tutti i tipi. <br/></p>
<blockquote>
[!Note]<br />
Esistono tre differenze tra i valori di tipo percepito e i valori per show. Per <code>show</code> , usare ' Documents ' anziché' doc ',' Pictures ' anziché' Pics ' è textdocuments ' anziché' text '.
</blockquote>
<p><br/></p></li>
<li>query: specifica i criteri di ricerca. Questo valore supporta i parametri della <a href="-search-2x-wds-aqsreference.md">sintassi di query avanzati</a> per affinare i risultati. Il parametro di query deve essere l'ultimo parametro nell'URL.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Esempio

Per cercare, ad esempio, tutti i file per le immagini corrispondenti al criterio ' Wallpaper ', utilizzare il comando seguente:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

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

 

 






---
title: Chiamata di WDS dalla riga di comando
description: È possibile avviare l'interfaccia utente di Microsoft Windows Desktop Search (WDS) con un filtro, un archivio e una query specifici da un'altra applicazione o da una pagina Web che usa l'oggetto browser helper (THEO) usando la sintassi della riga di comando di windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ba9fa8310af43340ef71c5d7e574f1b95addca86a4f90051dc85f593f43302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753217"
---
# <a name="calling-wds-from-the-command-line"></a>Chiamata di WDS dalla riga di comando

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare [invece Windows ricerca.](../search/-search-3x-wds-overview.md)

È possibile avviare l'interfaccia utente di Microsoft Windows Desktop Search (WDS) con un filtro, un archivio e una query specifici da un'altra applicazione o da una pagina Web che usa l'oggetto browser helper (THEO) usando la sintassi della riga di comando di windowssearch.exe. Quando si chiama Servizi di distribuzione Windows dalla riga di comando, nessuna informazione sulle azioni o sulla selezione dell'utente nella finestra di Servizi di distribuzione Windows viene restituita all'applicazione o alla pagina Web chiamante.

Il percorso di installazione di Servizi di distribuzione Windows viene specificato nell'impostazione del Registro di sistema InstallDir HKEY_LOCAL_MACHINE \\ Software Microsoft Windows Desktop \\ \\ Search. Il percorso predefinito in cui windowssearch.exe è installato è Programmi \\ Windows Desktop Search.

## <a name="command-line-syntax"></a>Sintassi della riga di comando

La sintassi seguente si applica all Windows della riga di comando di Ricerca desktop 2.x.



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
<td>/startup</td>

<td>Inizializza Windows Desktop Search</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Disattiva il back-off dell'indicizzazione e rielizza tutte le posizioni degli indici</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Mostra la finestra di stato dell'indicizzazione</td>
</tr>
<tr class="even">
<td>/launchsearchwindow o /url</td>

<td>Apre una finestra di Servizi di distribuzione Windows con una query vuota</td>
</tr>
<tr class="odd">
<td>/url</td>
<td>stringa di query search:[store|show|query]</td>
<td>Apre una finestra di Servizi di distribuzione Windows con una query e un filtro in base ai parametri seguenti:
<ul>
<li><p>store: specifica l'origine dati su cui eseguire la query: file, outlook, outlookexpress. Se non specificato, verrà cercata in tutti gli archivi. <br/></p>
<blockquote>
[!Note]<br />
Anche se la sintassi di query avanzata supporta il riferimento a Microsoft Outlook come 'oe', il parametro store nella riga di comando deve essere 'outlookexpress'.
</blockquote>
<p><br/></p></li>
<li><p>show: specifica il tipo percepito di risultati da restituire. Per <a href="-search-2x-wds-perceivedtype.md">un elenco completo dei tipi,</a> vedere Tipi percepiti. Se non specificato, verranno restituiti tutti i tipi. <br/></p>
<blockquote>
[!Note]<br />
Esistono tre differenze tra i valori del tipo percepito e i valori per show. Per <code>show</code> , usare "documents" anziché "doc", "pictures" anziché "pics" e "textdocuments" anziché "text".
</blockquote>
<p><br/></p></li>
<li>query: specifica i criteri di ricerca. Questo valore supporta i parametri <a href="-search-2x-wds-aqsreference.md">advanced query syntax</a> per perfezionare i risultati. Il parametro di query deve essere l'ultimo parametro nell'URL.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Esempio

Ad esempio, per cercare in tutti i file immagini corrispondenti ai criteri "sfondo" usare il comando seguente:

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

 

 






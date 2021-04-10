---
title: Uso delle macro per la gestione degli errori
description: COM definisce diverse macro che semplificano l'utilizzo dei valori HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730423"
---
# <a name="using-macros-for-error-handling"></a>Uso delle macro per la gestione degli errori

COM definisce diverse macro che semplificano l'utilizzo dei valori **HRESULT** .

Nella tabella seguente sono descritte le macro di gestione degli errori.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Macro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br/></td>
<td>Restituisce un valore <strong>HRESULT</strong> dato il bit di gravità, il codice della struttura e il codice di errore che comprendono <strong>HRESULT</strong>.<br/>
<blockquote>
[!Note]<br />
La chiamata di <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> per la verifica S_OK comporta una riduzione delle prestazioni. Per ottenere risultati ottimali, è consigliabile non utilizzare periodicamente <strong>MAKE_HRESULT</strong> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br/></td>
<td>Restituisce un oggetto <strong>SCODE</strong> dato il bit di gravità, il codice della struttura e il codice di errore che comprendono <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br/></td>
<td>Estrae la parte relativa al codice di errore del valore <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br/></td>
<td>Estrae il codice di struttura del valore <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br/></td>
<td>Estrae il bit di gravità del valore <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br/></td>
<td>Estrae la parte relativa al codice di errore di <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br/></td>
<td>Estrae il codice di struttura di <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br/></td>
<td>Estrae il campo di gravità di <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>COMPLETATA</strong></a><br/></td>
<td>Verifica il bit di gravità di <strong>SCODE</strong> o <strong>HRESULT</strong>; restituisce <strong>true</strong> se il livello di gravità è zero e <strong>false</strong> se è uno.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FALLITO</strong></a><br/></td>
<td>Verifica il bit di gravità di <strong>SCODE</strong> o <strong>HRESULT</strong>; restituisce <strong>true</strong> se il livello di gravità è uno e <strong>false</strong> se è zero.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br/></td>
<td>Fornisce un test generico per gli errori relativi a qualsiasi valore di stato. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br/></td>
<td>Esegue il mapping di un <a href="/windows/desktop/Debug/system-error-codes">codice di errore di sistema</a> a un valore <strong>HRESULT</strong> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br/></td>
<td>Esegue il mapping di un valore di stato di NT a un valore <strong>HRESULT</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 


---
description: Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966239"
---
# <a name="d3dcreate"></a>D3DCREATE

Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definire</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>L'applicazione chiede al dispositivo di guidare tutte le intestazioni di proprietà dell'adapter master. Il flag non è valido per gli adapter non master. Se questo flag è impostato, i parametri di presentazione passati a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> devono puntare a una matrice di <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>. Il numero di elementi in <strong>D3DPRESENT_PARAMETERS</strong> deve essere uguale al numero di schede definito dal membro NumberOfAdaptersInGroup della struttura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> . Il runtime di DirectX assegnerà ogni elemento a ogni intestazione nell'ordine numerico specificato dal membro AdapterOrdinalInGroup di <strong>D3DCAPS9</strong>.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D gestirà le risorse al posto del driver. Le chiamate Direct3D non avranno esito negativo per errori di risorse, ad esempio memoria video insufficiente.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Come D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D gestirà le risorse al posto del driver. A differenza di D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX restituirà errori per le condizioni, ad esempio la memoria video insufficiente.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Fa in modo che il runtime non registri i tasti di scelta rapida per printscreen, Ctrl-Printscreen e Alt-Printscreen per acquisire il contenuto del desktop o della finestra. 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>Limitare il calcolo al thread principale dell'applicazione. Se il flag non è impostato, il runtime può eseguire l'elaborazione dei vertici software e altri calcoli nel thread di lavoro per migliorare le prestazioni nei sistemi a più processori. 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Windows XP e Windows Vista:<br/> Questo flag è disponibile in Windows Vista, Windows Server 2008 e Windows 7.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>Consente la raccolta di statistiche presenti sul dispositivo. Le chiamate a <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> restituiranno dati validi. 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_FPU_PRESERVE</td>
<td>Impostare la precisione per i calcoli a virgola mobile Direct3D sulla precisione usata dal thread chiamante. Se non si specifica questo flag, Direct3D esegue per impostazione predefinita la modalità round-to-precisione singola per due motivi:
<ul>
<li>La modalità a precisione doppia ridurrà le prestazioni di Direct3D.</li>
<li>Parti di Direct3D presupporre che le eccezioni di unità a virgola mobile siano mascherate; annullare il mascheramento di queste eccezioni può causare un comportamento indefinito.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Specifica l'elaborazione del vertice hardware.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Specifica l'elaborazione del vertice mista (software e hardware). Per Windows 10, versione 1607 e successive, non è consigliabile usare questa impostazione. Vedere D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Specifica l'elaborazione dei vertici software. Per Windows 10, versione 1607 e successive, non è consigliabile usare questa impostazione. Usare D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
A meno che l'elaborazione dei vertici hardware non sia disponibile, l'utilizzo dell'elaborazione dei vertici software non è consigliato in Windows 10, versione 1607 (e versioni successive) perché l'efficienza dell'elaborazione dei vertici software è stata notevolmente ridotta migliorando la sicurezza dell'implementazione.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Indica che l'applicazione richiede che Direct3D sia multithread safe. In questo modo un thread Direct3D assume la proprietà della <a href="/windows/desktop/Sync/critical-section-objects">sezione critica</a> globale con maggiore frequenza, che può influire negativamente sulle prestazioni. Se un'applicazione elabora i messaggi della finestra in un thread durante l'esecuzione di chiamate API Direct3D in un altro thread, l'applicazione deve usare questo flag durante la creazione del dispositivo. Questa finestra deve anche essere eliminata prima di scaricare d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Indica che Direct3D non deve modificare la finestra di stato attivo in alcun modo.
<div class="alert">
<blockquote>
[!Note]<br />
Se questo flag è impostato, l'applicazione deve supportare completamente tutti gli eventi di gestione dello stato attivo, ad esempio gli eventi ALT + TAB e clic del mouse.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Specifica che Direct3D non supporta le chiamate Get * per qualsiasi elemento che può essere archiviato nei blocchi di stato. Indica inoltre a Direct3D di non fornire alcun servizio di emulazione per l'elaborazione dei vertici. Ciò significa che se il dispositivo non supporta l'elaborazione dei vertici, l'applicazione può usare solo i vertici post-trasformati.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Consente lo screen saver durante un'applicazione a schermo intero. Senza questo flag, Direct3D Disabilita gli screensaver fino a quando l'applicazione chiamante è a schermo intero. Se l'applicazione chiamante è già un salvaschermo, questo flag non ha alcun effetto. 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

D3DCREATE \_ hardware \_ VERTEXPROCESSING, D3DCREATE \_ mixed \_ VERTEXPROCESSING e D3DCREATE \_ software VERTEXPROCESSING \_ sono flag che si escludono a vicenda. È necessario specificare almeno uno di questi flag di elaborazione dei vertici quando si chiama [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | D3D9. h     |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

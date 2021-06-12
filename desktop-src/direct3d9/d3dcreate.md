---
description: Vedere una combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo nella costante D3DCREATE.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c24529c725b8b7c7f71c53718d56ceb50603
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011284"
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
<td>#Definire</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>L'applicazione chiede al dispositivo di guidare tutte le teste di proprietà dell'adattatore master. Il flag non è valido per gli adattatori non master. Se questo flag è impostato, i parametri di presentazione passati a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> devono puntare a una matrice <a href="d3dpresent-parameters.md"><strong>di</strong></a>D3DPRESENT_PARAMETERS . Il numero di elementi in <strong>D3DPRESENT_PARAMETERS</strong> deve essere uguale al numero di adattatori definiti dal membro NumberOfAdaptersInGroup della struttura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9.</strong></a> Il runtime DirectX assegna ogni elemento a ogni head nell'ordine numerico specificato dal membro AdapterOrdinalInGroup <strong>di D3DCAPS9.</strong></td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D gestirà le risorse anziché il driver. Le chiamate Direct3D non avranno esito negativo per errori delle risorse, ad esempio memoria video insufficiente.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Come D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D gestirà le risorse anziché il driver. A D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX restituirà errori per condizioni come memoria video insufficiente.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Fa in modo che il runtime non registri i tasti di scelta rapida per Printscreen, Ctrl-Printscreen e Alt-Printscreen per acquisire il contenuto del desktop o della finestra. 
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
<td>Abilita la raccolta delle statistiche presenti nel dispositivo. Le chiamate <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>a GetPresentStatistics</strong></a> restituiscono dati validi. 
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
<td>Impostare la precisione per i calcoli a virgola mobile Direct3D sulla precisione usata dal thread chiamante. Se non si specifica questo flag, direct3D viene impostato per impostazione predefinita sulla modalità round-to-nearest a precisione singola per due motivi:
<ul>
<li>La modalità a precisione doppia ridurrà le prestazioni direct3D.</li>
<li>Parti di Direct3D presuppongono che le eccezioni di unità a virgola mobile siano mascherate; L'annullamento del mascheramento di queste eccezioni può comportare un comportamento non definito.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Specifica l'elaborazione dei vertici hardware.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Specifica l'elaborazione mista dei vertici (software e hardware). Per Windows 10 versione 1607 e successive, non è consigliabile usare questa impostazione. Vedere D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Specifica l'elaborazione dei vertici software. Per Windows 10 versione 1607 e successive, non è consigliabile usare questa impostazione. Usare D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
A meno che l'elaborazione dei vertici hardware non sia disponibile, l'utilizzo dell'elaborazione dei vertici software non è consigliato in Windows 10, versione 1607 (e versioni successive) perché l'efficienza dell'elaborazione dei vertici software è stata notevolmente ridotta, migliorando al tempo stesso la sicurezza dell'implementazione.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Indica che l'applicazione richiede che Direct3D sia protetto da multithreading. In questo modo un thread Direct3D diventa più frequentemente proprietario della sezione critica <a href="/windows/desktop/Sync/critical-section-objects">globale,</a> con un possibile peggioramento delle prestazioni. Se un'applicazione elabora messaggi di finestra in un thread durante l'esecuzione di chiamate api Direct3D in un altro, l'applicazione deve usare questo flag durante la creazione del dispositivo. Questa finestra deve essere anche distrutta prima di scaricare d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Indica che Direct3D non deve modificare in alcun modo la finestra dello stato attivo.
<div class="alert">
<blockquote>
[!Note]<br />
Se questo flag è impostato, l'applicazione deve supportare completamente tutti gli eventi di gestione dello stato attivo, ad esempio ALT+TAB e gli eventi clic del mouse.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Specifica che Direct3D non supporta chiamate Get* per qualsiasi elemento che può essere archiviato in blocchi di stato. Indica inoltre a Direct3D di non fornire servizi di emulazione per l'elaborazione dei vertici. Ciò significa che se il dispositivo non supporta l'elaborazione dei vertici, l'applicazione può usare solo vertici post-trasformati.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Consente gli screensaver durante un'applicazione a schermo intero. Senza questo flag, Direct3D disabilita gli screensaver per tutto il tempo in cui l'applicazione chiamante è a schermo intero. Se l'applicazione chiamante è già uno screensaver, questo flag non ha alcun effetto. 
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



 

D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING, D3DCREATE \_ MIXED \_ VERTEXPROCESSING e D3DCREATE SOFTWARE VERTEXPROCESSING sono flag che si \_ \_ escludono a vicenda. Quando si chiama [**CreateDevice,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)è necessario specificare almeno uno di questi flag di elaborazione dei vertici.

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         |  Valore          |
|--------------------------|------------|
| Intestazione                   | D3D9.h     |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

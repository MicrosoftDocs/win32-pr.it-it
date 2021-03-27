---
title: Novità dell'SDK di agosto 2009 per Windows 7/Direct3D 11
description: Questa versione di Windows 7/Direct3D 11 viene fornita come parte di DirectX SDK e contiene nuove funzionalità, strumenti e documentazione.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731559"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>Novità dell'SDK di agosto 2009 per Windows 7/Direct3D 11

Questa versione di Windows 7/Direct3D 11 viene fornita come parte di DirectX SDK e contiene nuove funzionalità, strumenti e documentazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>Direct2D è un'API grafica 2D, con accelerazione immediata e in modalità immediata, che offre prestazioni elevate e rendering di elevata qualità per la geometria 2D, le bitmap e il testo. L'API Direct2D è progettata per interagire correttamente con Direct3D e GDI. Questo SDK consente agli sviluppatori di valutare l'API e scrivere semplici applicazioni, con alcune delle funzionalità più avanzate possibile nei computer configurati correttamente. <br/> La <a href="/windows/win32/direct2d/direct2d-portal">documentazione</a> e gli <a href="/previous-versions//dd372354(v=vs.85)">esempi</a> per Direct2D sono attualmente disponibili su MSDN.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite fornisce il supporto per il rendering di testo di alta qualità, i tipi di carattere di struttura indipendenti dalla risoluzione, il supporto completo per testo e layout Unicode e molto altro ancora:<br/>
<ul>
<li>Sistema di layout del testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.<br/></li>
<li>Rendering di testo di alta qualità, sottopixel e ClearType in grado di utilizzare GDI Direct3D, Direct2D o la tecnologia di rendering specifica dell'applicazione.<br/></li>
<li>Supporto per il testo in più formati. <br/></li>
<li>Supporto per le funzionalità tipografiche avanzate dei tipi di carattere OpenType.<br/></li>
<li>Supporto per il layout e il rendering del testo in tutte le lingue supportate da Windows.<br/></li>
</ul>
Questo SDK consente agli sviluppatori di valutare l'API e scrivere applicazioni di base solo a scopo dimostrativo.<br/> <a href="/windows/win32/directwrite/direct-write-portal">Documentazione</a> ed <a href="/windows/win32/directwrite/samples">esempi</a> per DirectWrite sono attualmente disponibili su MSDN.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1<br/></td>
<td><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1,1</a> si basa su DXGI 1,0 e sarà disponibile sia in Windows Vista che in Windows 7. DXGI 1,1 aggiunge diverse nuove funzionalità:<br/>
<ul>
<li>Supporto delle superfici condivise sincronizzate. Ciò consente una condivisione efficiente della superficie di lettura e scrittura tra più dispositivi D3D (potrebbe essere compreso tra D3D10 e D3D11).<br/></li>
<li>Supporto del formato BGRA. In questo modo è possibile eseguire il rendering di GDI nella stessa superficie DXGI di destinazione di un dispositivo Direct2D, Direct3D 10,1 o Direct3D 11. <br/></li>
<li>Latenza massima del frame. Utilizzando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: SetMaximumFrameLatency</strong></a> e <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: GetMaximumFrameLatency</strong></a>, i titoli possono controllare il numero di frame che possono essere archiviati in una coda, prima dell'invio per il rendering. La latenza viene spesso utilizzata per controllare il modo in cui la CPU sceglie di rispondere all'input dell'utente e ai frame presenti nella coda di rendering.<br/></li>
<li>Enumerazione dell'adapter. Se si usa <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>, i titoli possono enumerare le schede locali senza i monitoraggi o gli output collegati, nonché gli adapter con output collegati.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Esempi aggiornati<br/></td>
<td>Questa versione include alcuni esempi nuovi e aggiornati.<br/>
<ul>
<li>Il nuovo <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> è un'illustrazione di tecniche di elaborazione shader più avanzate che possono essere eseguite su una GPU D3D10 o d3d11.</li>
<li>L' <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">esempio HDRToneMappingCS11</a> è stato espanso per implementare gli effetti sfocatura e Bloom (oltre al mapping dei toni) usando compute shader, oltre a fornire pixel shader implementazioni per il confronto.</li>
<li>L' <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">esempio MultithreadedRendering11</a> è stato aggiornato in modo significativo, con risorse dell'arte più complesse e l'elaborazione per thread più intensiva.</li>
<li>L' <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">esempio SubD11</a> è stato aggiornato con un nuovo modello facciale e l'esempio USA ora la funzionalità di calcolo adiacenza dell'utilità di esportazione dei contenuti degli esempi.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità introdotte nelle versioni precedenti](d3d11-features-introduced-previous-releases.md)
</dt> </dl>


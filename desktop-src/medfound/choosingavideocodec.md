---
description: Scelta di un codec video
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Scelta di un codec video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b560666ddeebb88fc3bb720cbc9f1be26308e7ecd8a4ad872fbb1f0991826fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035369"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Scelta di un codec video (Microsoft Media Foundation)

Il Windows Media Video 9 Encoder supporta tre categorie di output codificato: Profilo principale, Profilo avanzato e Immagine. La categoria Profilo principale fornisce la compressione video generale per contenuti video complessi, ad esempio film o video musicali. Le funzionalità del profilo principale forniscono un'ampia gamma di impostazioni di codifica. È possibile usare il profilo principale per creare video con velocità in bit molto basse per la distribuzione su dispositivi portatili o, all'altra estremità dello spettro, è possibile usarlo per creare video ad alta definizione per il cinema digitale.

L'enfasi degli algoritmi di codifica nel profilo principale è il contenuto video dinamico, ma sono adatti anche per altri contenuti video. Il profilo principale deve essere la categoria predefinita per il contenuto video. Per soddisfare esigenze specifiche, è possibile usare la categoria Profilo avanzato, la categoria Immagine o un codificatore separato denominato codificatore dello schermo Windows Media Video 9. Nella tabella seguente sono elencate le quattro opzioni.



<table>
<thead>
<tr class="header">
<th>Scopo</th>
<th>Codec</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Codifica video per utilizzo generico</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificatore video multimediale 9</a><dl> Main Profile<br />
</dl></td>
</tr>
<tr class="even">
<td>Codifica di video o video ad alta definizione conformi allo standard VC-1 Advanced Profile SMPTE</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificatore video multimediale 9</a><dl> Profilo avanzato<br />
</dl></td>
</tr>
<tr class="odd">
<td>Conversione di immagini bitmap in video dinamico</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificatore video multimediale 9</a><dl> Immagine<br />
</dl></td>
</tr>
<tr class="even">
<td>Codificare il video dell'applicazione computer (acquisizione schermo) o un altro video altamente statico</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Windows Codificatore di schermo Media Video 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 




---
description: Scelta di un codec video
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Scelta di un codec video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225833"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Scelta di un codec video (Microsoft Media Foundation)

Il codificatore Windows Media Video 9 supporta tre categorie di output codificato: profilo principale, profilo avanzato e immagine. La categoria principale del profilo offre una compressione video generale per contenuti video complessi, ad esempio film o video musicali. Le funzionalità del profilo principale forniscono un'ampia gamma di impostazioni di codifica. È possibile usare il profilo principale per creare video con velocità in bit molto bassa per il recapito nei dispositivi palmari o, all'altra estremità dello spettro, è possibile usarlo per creare video ad alta definizione per Digital Cinema.

L'enfasi degli algoritmi di codifica nel profilo principale è il contenuto video dinamico, ma sono adatti anche per altri contenuti video. Il profilo principale deve essere la categoria predefinita per il contenuto video. Per soddisfare esigenze specifiche, è possibile usare la categoria di profili avanzati, la categoria di immagini o un codificatore separato denominato codificatore Windows Media Video 9. Nella tabella seguente sono elencate le quattro opzioni disponibili.



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
<td><a href="windowsmediavideo9encoder.md">Codificatore Windows Media Video 9</a><dl> Main Profile<br />
</dl></td>
</tr>
<tr class="even">
<td>Codifica di video o video ad alta definizione conformi allo standard VC-1 Advanced Profile SMPTE</td>
<td><a href="windowsmediavideo9encoder.md">Codificatore Windows Media Video 9</a><dl> Profilo avanzato<br />
</dl></td>
</tr>
<tr class="odd">
<td>Conversione di immagini bitmap in video dinamici</td>
<td><a href="windowsmediavideo9encoder.md">Codificatore Windows Media Video 9</a><dl> Immagine<br />
</dl></td>
</tr>
<tr class="even">
<td>Codifica del computer-video dell'applicazione (acquisizione schermo) o altro video altamente statico</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Codificatore dello schermo Windows Media Video 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 




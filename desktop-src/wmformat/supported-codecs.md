---
title: Codec supportati
description: Codec supportati
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Media Format SDK, codec supportati
- Windows Media Format SDK, interfaccia IWMCodecInfo3
- codec, supportati
- IWMCodecInfo3, informazioni
- codec, interfaccia IWMCodecInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723590"
---
# <a name="supported-codecs"></a>Codec supportati

Windows Media Format SDK fornisce il supporto per i codec seguenti, inclusi quando si installa l'SDK.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codec</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Media Audio</td>
<td>Codec audio per l'uso generale nella codifica di audio complessi, come la musica. Le versioni più recenti di questo codec sono il codec Windows Media Audio 9 e il codec Windows Media Audio 9,1.<br/></td>
</tr>
<tr class="even">
<td>Windows Media Audio Professional</td>
<td>Codec audio per audio complesso, ad esempio Music. Supporta la codifica multicanale e a 24 bit. Sono disponibili due versioni di questo codec:<br/>
<ul>
<li>Windows Media Audio 9 Professional</li>
<li>Windows Media Audio 9,1 Professional</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows Media Audio senza perdita di perdite</td>
<td>Codec audio per la codifica senza perdita di contenuti. Sono disponibili due versioni di questo codec:<br/>
<ul>
<li>Windows Media Audio 9 senza perdita di perdite</li>
<li>Windows Media Audio 9,1 senza perdita di perdite</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Media Audio 9 Voice</td>
<td>Codec audio ottimizzato per la codifica della voce umana a rapporti di compressione elevati. Questo è il codec preferito per i flussi costituiti principalmente da parole vocali. Per contenuti con musica mista e sintesi vocale, questo codec può modificare dinamicamente l'algoritmo di codifica usato per ottenere la qualità ottimale.</td>
</tr>
<tr class="odd">
<td>Windows Media Video 9</td>
<td>Codec video per l'uso generale nel video di codifica complesso, ad esempio i film.</td>
</tr>
<tr class="even">
<td>Profilo avanzato Windows Media Video 9</td>
<td>Codec video che incorpora le funzionalità di codifica avanzata, inclusa la codifica interlacciata.</td>
</tr>
<tr class="odd">
<td>Schermata Windows Media Video 9</td>
<td>Codec video ottimizzato per la codifica di schermate sequenziali. Questo codec viene spesso usato per il training o il supporto software registrando le immagini di monitoraggio quando vengono usate le applicazioni computer.</td>
</tr>
<tr class="even">
<td>Immagine di Windows Media Video</td>
<td>Codec video per la conversione di immagini bitmap con informazioni di deformazione nel video compresso. Sono disponibili due versioni di questo codec:<br/>
<ul>
<li>Immagine di Windows Media Video 9</li>
<li>Windows Media Video 9 immagine v2</li>
</ul></td>
</tr>
</tbody>
</table>



 

Sono disponibili versioni diverse dei codec Windows Media Audio e video per la codifica a seconda della versione di Windows Media Format SDK installata. Quando si usano i metodi se l'interfaccia [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) per enumerare codec e formati di codec, vengono enumerate solo le versioni più recenti supportate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scelta di un metodo di codifica**](choosing-an-encoding-method.md)
</dt> <dt>

[**Funzionalità di codec**](codec-features.md)
</dt> </dl>

 

 






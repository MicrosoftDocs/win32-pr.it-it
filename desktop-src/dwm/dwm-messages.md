---
title: Messaggi DWM
description: In questa sezione vengono fornite informazioni sui messaggi di Gestione finestre desktop (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Gestione finestre desktop (DWM), riferimento
- DWM (Gestione finestre desktop), riferimento
- Gestione finestre desktop (DWM), messaggi
- DWM (Gestione finestre desktop), messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299359"
---
# <a name="dwm-messages"></a>Messaggi DWM

In questa sezione vengono fornite informazioni sui messaggi di Gestione finestre desktop (DWM).

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a><br/></td>
<td>Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a><br/></td>
<td>Informa tutte le finestre di primo livello che la composizione di DWM è stata abilitata o disabilitata. <br/>
<blockquote>
[!Note]<br />
A partire da Windows 8, la composizione di DWM è sempre abilitata, quindi questo messaggio non viene inviato indipendentemente dalle modifiche della modalità video.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a><br/></td>
<td>Inviato quando i criteri di rendering dell'area non client vengono modificati.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a><br/></td>
<td>Indica a una finestra di fornire una bitmap statica da utilizzare come <em>anteprima in tempo reale</em> (nota anche come <em>Anteprima di visualizzazione</em>) di tale finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a><br/></td>
<td>Indica a una finestra di fornire una bitmap statica da utilizzare come rappresentazione di anteprima di tale finestra.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a><br/></td>
<td>Inviato quando una finestra di DWM composta viene ingrandita.<br/></td>
</tr>
</tbody>
</table>



 

 

 






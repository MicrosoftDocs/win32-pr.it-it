---
description: Filtro overlay Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro overlay Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc521af700b7cbf80624483ff6820efda0704485fdcd9587c87733e6db6f3a7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501911"
---
# <a name="overlay-mixer-2-filter"></a>Filtro overlay Mixer 2

Il filtro Overlay Mixer 2 è identico al filtro [overlay Mixer, ad](overlay-mixer-filter.md) eccezione di:

-   Supporta solo tipi di supporti con [**formati VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)
-   Ha un maggior merito, che ne consente l'aggiunta automatica a un grafico di filtro.

L'Mixer 2 viene fornito in modo che Filter Graph Manager lo aggiungerà al grafo quando esegue il rendering di video MPEG-2 non DVD. La scelta di usare l'Mixer di sovrimpressione o la sovrimpressione Mixer 2 viene gestita dal componente che compila il grafo, da Filter Graph Manager, da Capture Graph Builder o da DVD Graph Builder. Dal punto di vista dell'applicazione, si tratta dello stesso filtro, con le stesse interfacce e funzionalità.

La tabella seguente contiene informazioni specifiche per la sovrimpressione Mixer 2. Per tutti gli altri dati di filtro, vedere la documentazione relativa alla sovrapposizione Mixer.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tipi di supporti pin di input</td>
<td>Tipo di formato: Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>CLSID del filtro</td>
<td>CLSID_OverlayMixer2</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td><ul>
<li>MERIT_UNLIKELY</li>
<li>Windows Vista o versioni successive: MERIT_DO_NOT_USE</li>
</ul></td>
</tr>
</tbody>
</table>



 

In Windows Vista o versioni successive, il merito del filtro Overlay Mixer 2 è LA NON USARE, perché i renderer video più nuovi \_ \_ \_ (VMR-7, VMR-9 ed EVR) supportano tutti i formati **VIDEOINFOHEADER2** e pertanto non è necessario usare i formati overlay Mixer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




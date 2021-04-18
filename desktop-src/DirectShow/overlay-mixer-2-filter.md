---
description: Filtro Overlay Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro Overlay Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304173"
---
# <a name="overlay-mixer-2-filter"></a>Filtro Overlay Mixer 2

Il filtro Overlay Mixer 2 è identico al filtro per il [mixer sovrapposto](overlay-mixer-filter.md) , ad eccezione di:

-   Supporta solo i tipi di supporto con formati [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Ha un merito più elevato, che consente di aggiungerlo a un grafico di filtro automaticamente.

Il mixer sovrapposto 2 viene fornito in modo che il gestore del grafico del filtro lo aggiunga al grafico durante il rendering del video MPEG-2 non DVD. La scelta di usare il mixer di sovrimpressione o il mixer sovrapposto 2 viene gestita dal componente che compila il grafo, ovvero il gestore del grafico del filtro, il generatore di grafici di acquisizione o il generatore di grafici DVD. Dal punto di vista dell'applicazione, si tratta dello stesso filtro, con le stesse interfacce e funzionalità.

La tabella seguente contiene informazioni specifiche per il mixer sovrapposto 2. Per tutti gli altri dati del filtro, fare riferimento alla documentazione per il mixer overlay.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tipi di supporti pin di input</td>
<td>Tipo formato: Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
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



 

In Windows Vista o versioni successive, il merito del filtro Overlay Mixer 2 è MERIT \_ non \_ \_ usare, perché i renderer video più recenti (VMR-7, VMR-9 e EVR) supportano tutti i formati **VIDEOINFOHEADER2** e pertanto non è necessario usare il mixer overlay.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




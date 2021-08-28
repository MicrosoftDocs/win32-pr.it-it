---
description: Filtro overlay Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro overlay Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b51dceb2a7f82a91fe30275cacfaad4ad78eded
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987354"
---
# <a name="overlay-mixer-2-filter"></a>Filtro overlay Mixer 2

Il filtro Overlay Mixer 2 è identico al filtro [Overlay Mixer,](overlay-mixer-filter.md) ad eccezione di:

-   Supporta solo tipi di supporti con [**formati VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)
-   Ha un merito più elevato, che ne consente l'aggiunta automatica a un grafo di filtro.

L'Mixer overlay 2 viene fornito in modo che Filter Graph Manager lo aggiungerà al grafico quando esegue il rendering di video MPEG-2 non DVD. La scelta di usare il Mixer Di sovrapposizione o overlay Mixer 2 viene gestita dal componente che compila il grafo, da Filter Graph Manager, da Capture Graph Builder o da DVD Graph Builder. Dal punto di vista dell'applicazione, sono lo stesso filtro, con le stesse interfacce e funzionalità.

La tabella seguente contiene informazioni specifiche per l'Mixer 2. Per tutti gli altri dati di filtro, vedere la documentazione relativa all'Mixer.




| Etichetta | Valore |
|--------|-------|
| Tipi di supporti pin di input | Tipo di formato: Format_VIDEOINFO2 | 
| Filtro CLSID | CLSID_OverlayMixer2 | 
| <a href="merit.md">Merito</a> | <ul><li>MERIT_UNLIKELY</li><li>Windows Vista o versione successiva: MERIT_DO_NOT_USE</li></ul> | 




 

In Windows Vista o versioni successive, il merito del filtro Overlay Mixer 2 è MERIT DO NOT USE, perché i renderer video più nuovi \_ \_ \_ (VMR-7, VMR-9 ed EVR) supportano tutti i formati **VIDEOINFOHEADER2** e pertanto non è necessario usare l'Mixer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




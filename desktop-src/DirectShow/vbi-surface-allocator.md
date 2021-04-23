---
description: Allocatore di superficie VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocatore di superficie VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909009"
---
# <a name="vbi-surface-allocator"></a>Allocatore di superficie VBI

L'allocatore di superficie VBI controlla l'allocazione dei buffer VBI nei grafici della tv analogica con scenari di acquisizione di porte video hardware. Con dispositivi come il decodificatore Bt829, il buffer frame può contenere più buffer di acquisizione VBI a cui si accede tramite un meccanismo proprietario basato su hardware noto genericamente come porta video. Il filtro VBI Surface Allocator si connette a valle dal filtro di acquisizione e non dispone di un pin di output. Il filtro funziona a stretto contatto con [il mixer](overlay-mixer-filter.md) di sovrapposizione (tramite DirectDraw) per eseguire operazioni coordinate sulla porta video hardware, utilizzando la stessa memoria buffer frame SVGA limitata.



| Label | Valore |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ VPVBI                                               |
| Interfacce pin di input                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Tipi di supporti pin di output                   | MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL. Al pin di output non è mai connesso nulla. |
| Interfacce pin di output                    | Non applicabile.                                                                     |
| Filtro CLSID                             | CLSID \_ VBISurfaces                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                   |
| File eseguibile                               | vbisurf.ax                                                                          |
| [Merito](merit.md)                       | MERIT \_ NORMAL                                                                       |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 




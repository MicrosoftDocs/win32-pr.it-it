---
description: Allocatore di superficie VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocatore di superficie VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c586c3ef135722ac259813d918dc4054617b8ae6bfb987083f0a2ceaa986067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071985"
---
# <a name="vbi-surface-allocator"></a>Allocatore di superficie VBI

L'allocatore di superficie VBI controlla l'allocazione dei buffer VBI nei grafici della tv analogica con scenari di acquisizione di porte video hardware. Con dispositivi come il decodificatore Bt829, il buffer dei frame può contenere più buffer di acquisizione VBI a cui si accede tramite un meccanismo proprietario basato su hardware noto genericamente come porta video. Il filtro VBI Surface Allocator si connette a valle dal filtro di acquisizione e non dispone di un pin di output. Il filtro funziona in stretta collaborazione con [l'Mixer](overlay-mixer-filter.md) overlay (tramite DirectDraw) per eseguire operazioni coordinate sulla porta video hardware, utilizzando la stessa memoria buffer frame SVGA limitata.



| Etichetta | Valore |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ VPVBI                                               |
| Interfacce pin di input                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Tipi di supporti pin di output                   | MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL. Al pin di output non è mai connesso nulla. |
| Interfacce pin di output                    | Non applicabile.                                                                     |
| Filtro CLSID                             | CLSID \_ VBISurfaces                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                   |
| File eseguibile                               | vbisurf.ax                                                                          |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                                       |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




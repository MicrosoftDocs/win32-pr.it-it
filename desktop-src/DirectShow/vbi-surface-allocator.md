---
description: Allocatore di superficie VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocatore di superficie VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757676"
---
# <a name="vbi-surface-allocator"></a>Allocatore di superficie VBI

VBI Surface allocator controlla l'allocazione dei buffer VBI nei grafici della televisione analogica con scenari di acquisizione della porta video hardware. Con i dispositivi come il decodificatore BT829, il buffer del frame può contenere più buffer di acquisizione VBI a cui si accede tramite un meccanismo proprietario basato su hardware noto in modo generico come porta video. Il filtro VBI Surface allocator si connette a valle dal filtro di acquisizione e non ha un pin di output. Il filtro opera a stretto contatto con il [mixer overlay](overlay-mixer-filter.md) (tramite DirectDraw) per eseguire operazioni coordinate sulla porta video hardware, usando la stessa memoria limitata del buffer di frame SVGA.



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Tipi di supporti pin di input                    | \_Video di MEDIATYPE, MEDIASUBTYPE \_ VPVBI                                               |
| Interfacce pin di input                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Tipi di supporti pin di output                   | MEDIATYPE \_ null, MEDIASUBTYPE \_ null. (Nessun elemento è mai connesso al pin di output). |
| Interfacce del PIN di output                    | Non applicabile.                                                                     |
| CLSID filtro                             | \_VBISURFACES CLSID                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                   |
| File eseguibile                               | vbisurf.ax                                                                          |
| [Merito](merit.md)                       | VALORE \_ normale                                                                       |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




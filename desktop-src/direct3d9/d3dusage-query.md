---
description: Queste opzioni identificano i tipi di risorse di query.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994108"
---
# <a name="d3dusage_query"></a>D3DUSAGE \_ QUERY

Queste opzioni identificano i tipi di risorse di query.



| \#Definire                                   | Descrizione                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTRO QUERY D3DUSAGE \_ \_                    | Eseguire una query sul formato della risorsa per verificare se supporta tipi di filtro trame diversi da D3DTEXF \_ POINT (che è sempre supportato).                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP             | Eseguire una query sulla risorsa su una mappa di rilievo legacy.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING | Eseguire una query sulla risorsa per verificare il supporto per il supporto pixel shader blending. Se [**CheckDeviceFormat ha**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) esito negativo con D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING, le operazioni di fusione post-pixel non sono supportate. Sono inclusi il test alfa, la nebbia dei pixel, la fusione della destinazione di rendering, l'abilitazione della scrittura dei colori e il dithering. |
| D3DUSAGE \_ QUERY \_ SRGBREAD                  | Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di lettura.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ QUERY \_ SRGBWRITE                 | Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di scrittura.                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ QUERY \_ VERTEXTEXTURE             | Eseguire una query sulla risorsa per verificare il supporto per il campionamento delle trame dei vertex shader.                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ QUERY \_ WRAPANDMIP                | Eseguire una query sulla risorsa per verificare il supporto per il wrapping delle trame e il mapping mip.                                                                                                                                                                                                                                                                          |



 

Usare [**CheckDeviceFormat per**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) eseguire query sul supporto hardware per questi utilizzi e su altri utilizzi elencati in [D3DUSAGE](d3dusage.md).

## <a name="constant-information"></a>Informazioni costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3d9types.h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

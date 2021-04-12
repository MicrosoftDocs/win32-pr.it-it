---
description: Queste opzioni identificano i tipi di risorse della query.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126878"
---
# <a name="d3dusage_query"></a>\_Query D3DUSAGE

Queste opzioni identificano i tipi di risorse della query.



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                                   | Descrizione                                                                                                                                                                                                                                                                                                                                         |
| \_Filtro query \_ D3DUSAGE                    | Eseguire una query sul formato di risorsa per verificare se supporta i tipi di filtro di trama diversi dal punto di D3DTEXF, \_ che è sempre supportato.                                                                                                                                                                                                                         |
| \_LEGACYBUMPMAP query \_ D3DUSAGE             | Eseguire una query sulla risorsa relativa a una mappa Bump legacy.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ query \_ POSTPIXELSHADER \_ blending | Eseguire una query sulla risorsa per verificare il supporto per il supporto di post pixel shader blending. Se [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) ha esito negativo con D3DUSAGE \_ query \_ POSTPIXELSHADER \_ blending, le operazioni successive alla fusione dei pixel non sono supportate. Sono inclusi test alfa, nebbia pixel, Blend di destinazione di rendering, abilitazione della scrittura di colori e dithering. |
| \_SRGBREAD query \_ D3DUSAGE                  | Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di lettura.                                                                                                                                                                                                                                                        |
| \_SRGBWRITE query \_ D3DUSAGE                 | Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di scrittura.                                                                                                                                                                                                                                                       |
| \_VERTEXTEXTURE query \_ D3DUSAGE             | Eseguire una query sulla risorsa per verificare il supporto per il campionamento di trama vertex shader.                                                                                                                                                                                                                                                                            |
| \_WRAPANDMIP query \_ D3DUSAGE                | Eseguire una query sulla risorsa per verificare il supporto per il wrapping della trama e il mapping MIP.                                                                                                                                                                                                                                                                          |



 

Usare [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) per eseguire query sul supporto hardware per questi usi e altri utilizzi elencati in [D3DUSAGE](d3dusage.md).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3d9types. h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

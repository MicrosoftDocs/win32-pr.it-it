---
description: Flag di funzionalità delle coordinate della trama del driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f954020f80a8c980316e71f22f75ad47616e071d460d1c4a6c13e762ab3df462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750601"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Flag di funzionalità delle coordinate della trama del driver.



| \#Definire                                 | Valore       | Descrizione                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | Usare le coordinate di trama specificate contenute nel formato vertice. Questo valore viene risolto in zero.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Usare la normale vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinata di trama di input per la trasformazione della trama di questa fase. Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Usare le coordinate di trama specificate per il mapping della sfera.                                                                                                                                                            |



 

Queste costanti vengono usate da D3DTSS \_ TEXCOORDINDEX.

## <a name="constant-information"></a>Informazioni costanti



|  Requisito                        | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




---
description: Flag della funzionalità di coordinate della trama del driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966315"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Flag della funzionalità di coordinate della trama del driver.



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                                 | Valore       | Descrizione                                                                                                                                                                                                          |
| D3DTSS \_ TCI \_ PassThru                    | 0x00000000L | Usare le coordinate di trama specificate contenute all'interno del formato del vertice. Questo valore viene risolto in zero.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Usare il vertice normale, trasformato nello spazio della fotocamera, come coordinate di trama di input per la trasformazione di trama di questa fase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate di trama di input per la trasformazione di trama di questa fase.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinata di trama di input per la trasformazione di trama di questa fase. Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Usare le coordinate di trama specificate per il mapping della sfera.                                                                                                                                                            |



 

Queste costanti vengono usate da D3DTSS \_ TEXCOORDINDEX.

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




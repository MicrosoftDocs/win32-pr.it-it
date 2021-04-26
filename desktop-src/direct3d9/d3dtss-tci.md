---
description: Flag di funzionalità delle coordinate della trama del driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995258"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Flag di funzionalità delle coordinate della trama del driver.



| \#Definire                                 | Valore       | Descrizione                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | Usare le coordinate di trama specificate contenute nel formato vertice. Questo valore viene risolto in zero.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Usa la normale del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Usa la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinata della trama di input per la trasformazione della trama di questa fase. Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale. |
| MAPPA \_ SPHEREMAP TCI D3DTSS \_                   | 0x00040000L | Usare le coordinate di trama specificate per il mapping della sfera.                                                                                                                                                            |



 

Queste costanti vengono usate da D3DTSS \_ TEXCOORDINDEX.

## <a name="constant-information"></a>Informazioni costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




---
description: Costanti di limitazione delle risorse.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1d6bf4f72c4ef09eafba3ee50659e5e6ffc682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342271"
---
# <a name="d3d10_req"></a>\_Req D3D10

Costanti di limitazione delle risorse.



| \#definire                                      | Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Livelli MIP di D3D10 req \_                       | 14    | Numero massimo di livelli di mipmap che possono essere presenti in una risorsa di trama.                                                                                                                                                                                                                                                                                                                                                                    |
| \_ \_ Dimensioni della risorsa D3D10 req \_ \_ in \_ megabyte     | 128   | Dimensioni massime possibili di una risorsa in megabyte. Le app possono creare risorse maggiori delle dimensioni massime delle risorse in alcuni componenti hardware grafici. Tuttavia, è consigliabile che le applicazioni mantengano le risorse inferiori alle dimensioni massime della risorsa per ottenere la massima compatibilità tra i fornitori di grafica. Il runtime garantisce solo che le allocazioni nelle dimensioni massime delle risorse siano supportate da tutti i componenti hardware di Direct3D 10. |
| \_Dimensione dell' \_ \_ asse della matrice D3D10 req TEXTURE1D \_ \_ | 512   | Dimensione massima della matrice di una matrice di trama 1D.                                                                                                                                                                                                                                                                                                                                                                                       |
| \_Dimensione dell' \_ \_ asse della matrice D3D10 req TEXTURE2D \_ \_ | 512   | Dimensione massima della matrice di una matrice di trama 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| \_Dimensione D3D10 req \_ TEXTURE1D \_ U \_           | 8192  | Larghezza massima di una trama 1D.                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_Dimensione D3D10 req \_ TEXTURE2D \_ U \_ o \_ V \_    | 8192  | Larghezza e altezza massime di una trama 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| \_Dimensione D3D10 req \_ TEXTURE3D \_ U \_ V \_ o \_ W \_ | 2048  | Larghezza massima, altezza e profondità di una trama 3D.                                                                                                                                                                                                                                                                                                                                                                               |
| \_Dimensione D3D10 req \_ TEXTURECUBE \_            | 8192  | Dimensione massima di una trama del cubo.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Le costanti sono definite in D3D10. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti di risorsa](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Riferimento a Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 




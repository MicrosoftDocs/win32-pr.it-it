---
description: Costanti di limitazione delle risorse.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e099c26706772bbb76ad6709759fa4712e22ea3bc9793b905a2050f25d0f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100753"
---
# <a name="d3d10_req"></a>D3D10 \_ REQ

Costanti di limitazione delle risorse.



| \#Definire                                      | Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ REQ \_ MIP \_ LEVELS                       | 14    | Numero massimo di livelli di mipmap che possono avere una risorsa trama.                                                                                                                                                                                                                                                                                                                                                                    |
| DIMENSIONI DELLA RISORSA REQ D3D10 \_ \_ IN \_ \_ \_ MEGABYTE     | 128   | Dimensione massima possibile di una risorsa in megabyte. Le app possono creare risorse più grandi delle dimensioni massime delle risorse in alcuni componenti hardware grafici. Tuttavia, è consigliabile che le app mantenino le risorse inferiori alle dimensioni massime delle risorse per ottenere la massima compatibilità tra i fornitori di grafica. Il runtime garantisce solo che le allocazioni entro le dimensioni massime delle risorse siano supportate da tutto l'hardware Direct3D 10. |
| DIMENSIONE DELL'ASSE DELLA MATRICE \_ TEXTURE1D REQ \_ D3D10 \_ \_ \_ | 512   | Dimensione massima della matrice di una matrice di trame 1D.                                                                                                                                                                                                                                                                                                                                                                                       |
| DIMENSIONE DELL'ASSE DELLA MATRICE \_ \_ TEXTURE2D REQ \_ \_ D3D10 \_ | 512   | Dimensione massima della matrice di una matrice di trame 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| DIMENSIONE D3D10 \_ REQ \_ TEXTURE1D \_ U \_           | 8192  | Larghezza massima di una trama 1D.                                                                                                                                                                                                                                                                                                                                                                                                  |
| DIMENSIONE D3D10 \_ REQ \_ TEXTURE2D \_ U O \_ \_ \_ V    | 8192  | Larghezza e altezza massime di una trama 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| DIMENSIONE D3D10 \_ REQ \_ TEXTURE3D \_ U V O \_ \_ \_ W \_ | 2048  | Larghezza, altezza e profondità massime di una trama 3D.                                                                                                                                                                                                                                                                                                                                                                               |
| DIMENSIONE \_ TEXTURECUBE D3D10 \_ REQ \_            | 8192  | Dimensioni massime di una trama del cubo.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Le costanti sono definite in D3D10.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti di risorsa](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Informazioni di riferimento su Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 




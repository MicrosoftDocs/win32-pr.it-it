---
description: I parametri di nebbia sono controllati tramite gli Stati di rendering del dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parametri di nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876401"
---
# <a name="fog-parameters-direct3d-9"></a>Parametri di nebbia (Direct3D 9)

I parametri di nebbia sono controllati tramite gli Stati di rendering del dispositivo. I tipi di nebbia pixel e vertex supportano tutte le formule di nebbia introdotte nelle [formule di nebbia (Direct3D 9)](fog-formulas.md). Il tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) definisce le costanti che è possibile usare per identificare la formula di nebbia che si vuole venga usata da Microsoft Direct3D. Lo \_ stato di rendering FOGTABLEMODE di D3DRS controlla la modalità di nebbia utilizzata da Direct3D per la nebbia dei pixel e lo \_ stato di rendering FOGVERTEXMODE di D3DRS controlla la modalità per la nebbia dei vertici.

Quando si usa la formula di nebbia lineare, si impostano le distanze iniziale e finale tramite gli \_ Stati di rendering D3DRS FOGSTART e D3DRS \_ FOGEND. Il modo in cui i valori vengono interpretati dal sistema dipende dal tipo di nebbia usata dall'applicazione: la nebbia dei pixel o dei vertici e, quando si usa la nebbia dei pixel, se si usa la profondità basata su z o w. Nella tabella seguente sono riepilogati i tipi di nebbia e le rispettive unità di inizio e di fine.



| Tipo di nebbia  | Unità di inizio/fine nebbia      |
|-----------|--------------------------|
| Pixel (Z) | Spazio del dispositivo \[ 0,0, 1.0\] |
| Pixel (W) | Spazio fotocamera             |
| Vertice    | Spazio fotocamera             |



 

Lo \_ stato di rendering FOGDENSITY di D3DRS controlla la densità di nebbia applicata quando è abilitata una formula di nebbia esponenziale. La densità di nebbia è essenzialmente un fattore di ponderazione, compreso tra 0,0 e 1,0 (inclusi), che consente di ridimensionare il valore di distanza nell'esponente.

Il colore usato dal sistema per la fusione di nebbia viene controllato tramite lo \_ stato di rendering del dispositivo FogColor di D3DRS. Per altre informazioni, vedere [colore di nebbia (Direct3D 9)](fog-color.md) e [blending di nebbia (Direct3D 9)](fog-blending.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 

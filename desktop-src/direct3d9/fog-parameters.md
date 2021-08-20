---
description: I parametri di nebbia vengono controllati tramite gli stati di rendering del dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parametri di Nebbio (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c7883905e59c7147b94a2f803e7b5b74baeccf9383885fe49c69f2e1eeac87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094799"
---
# <a name="fog-parameters-direct3d-9"></a>Parametri di Nebbio (Direct3D 9)

I parametri di nebbia vengono controllati tramite gli stati di rendering del dispositivo. Entrambi i tipi di foschia pixel e vertice supportano tutte le formule di osanna introdotte nelle [formule di nebbia (Direct3D 9).](fog-formulas.md) Il [**tipo enumerato D3DFOGMODE**](./d3dfogmode.md) definisce le costanti che è possibile usare per identificare la formula della nebbia che si vuole usare da Microsoft Direct3D. Lo stato di rendering D3DRS FOGTABLEMODE controlla la modalità di nebbia utilizzata da Direct3D per la nebbia dei pixel e lo stato di \_ rendering D3DRS FOGVERTEXMODE controlla la modalità per la nebbia dei \_ vertici.

Quando si usa la formula osa lineare, si impostano le distanze iniziale e finale attraverso gli stati di rendering \_ D3DRS FOGSTART e D3DRS \_ FOGEND. Il modo in cui il sistema interpreta questi valori dipende dal tipo di osanna usata dall'applicazione - osanna pixel o vertice - e, quando si usa la nebbia pixel, se viene usata la profondità basata su z o w. Nella tabella seguente sono riepilogati i tipi di nebbia e le relative unità di inizio e fine.



| Tipo di nebbia  | Unità inizio/fine nebbia      |
|-----------|--------------------------|
| Pixel (Z) | Spazio del \[ dispositivo 0.0,1.0\] |
| Pixel (W) | Spazio della fotocamera             |
| Vertice    | Spazio della fotocamera             |



 

Lo stato di rendering D3DRS FOGDENSITY controlla la densità della nebbia applicata quando è abilitata una formula di \_ osanna esponenziale. La densità della nebbia è essenzialmente un fattore di ponderazione, compreso tra 0,0 e 1,0 (inclusi), che ridimensiona il valore della distanza nell'esponente.

Il colore utilizzato dal sistema per la fusione delle nebbie viene controllato tramite lo stato di rendering del dispositivo D3DRS \_ FOGCOLOR. Per altre informazioni, vedere [Colore fusto (Direct3D 9)](fog-color.md) e [Misto di fusi (Direct3D 9).](fog-blending.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 

---
title: Come inizializzare la fase mosaico
description: In questo argomento viene illustrato come inizializzare la fase mosaico.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992741"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Procedura: inizializzare la fase mosaico

In generale, la suddivisione a mosaico espande il modello compatto, definito dall'utente, di una patch in geometria che contiene una quantità programmabile di dettagli. La geometria è in genere un set di triangoli che rappresenta la geometria della superficie dettagliata. In questo argomento viene illustrato come inizializzare la fase mosaico.

La fase mosaico è la seconda delle tre fasi che interagiscono con conteggiarla suddividerla o affiancano una superficie. La prima fase è la fase Hull shader; funziona una volta per patch e configura il comportamento della fase successiva (funzione fissa mosaico). Uno scafo shader genera anche output definiti dall'utente, ad esempio punti di controllo di output e costanti di patch, che vengono inviati oltre il mosaico direttamente alla terza fase, ovvero la fase di shader del dominio. Un Domain shader viene richiamato una volta per ogni punto di mosaico e valuta le posizioni della superficie.

La fase mosaico è una fase di funzione fissa, non sono presenti shader da generare e nessun stato da impostare. Riceve tutto lo stato di installazione dalla fase dello scafo dello shader. una volta inizializzata la fase Hull shader, la fase mosaico viene inizializzata automaticamente.

**Per inizializzare la fase mosaico**

-   Inizializzare la fase Hull shader con [**sul ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances* è un puntatore a una matrice di interfacce dello shader, rappresentata da puntatori [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) e dal numero di interfacce, rappresentate da *NumClassInstances*. Se non viene usato, questi parametri possono essere impostati rispettivamente su **null** e 0.

Dopo l'inizializzazione della fase Hull shader, è necessario inizializzare anche la fase Domain-shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Panoramica dello schema a mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 





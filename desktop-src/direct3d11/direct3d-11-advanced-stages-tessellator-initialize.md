---
title: Come inizializzare la fase tessellator
description: In questo argomento viene illustrato come inizializzare la fase del tessellatore.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f842b1095a4053ad35838864bac6d6677194d85f48e0a78e2fc6975af1e3b8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096281"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Procedura: Inizializzare la fase tessellator

In generale, la struttura a tessellazione espande il modello compatto, definito dall'utente, di una patch in una geometria che contiene una quantità programmabile di dettagli. La geometria è in genere un set di triangoli che rappresenta la geometria dettagliata della superficie. In questo argomento viene illustrato come inizializzare la fase del tessellatore.

La fase a tessellatore è la seconda di tre fasi che lavorano insieme per affiancare o affiancare una superficie. La prima fase è la fase hull-shader. funziona una volta per ogni patch e configura il comportamento della fase successiva (il tessellatore di funzioni fisse). Uno hull shader genera anche output definiti dall'utente, ad esempio punti di controllo dell'output e costanti patch, che vengono inviati oltre il tessellatore direttamente alla terza fase, la fase domain-shader. Uno shader di dominio viene richiamato una volta per ogni punto della fase a tessellatore e valuta le posizioni della superficie.

La fase a tessellatore è una fase di funzione fissa, non è presente alcuno shader da generare e nessuno stato da impostare. Riceve tutto lo stato di configurazione dalla fase di hull shader. Dopo l'inizializzazione della fase di hull shader, la fase a tessellatore viene inizializzata automaticamente.

**Per inizializzare la fase del tessellatore**

-   Inizializzare la fase hull-shader [**usando ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances è* un puntatore a una matrice di interfacce shader, rappresentate da [**puntatori ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) e dal numero di interfacce, rappresentate da *NumClassInstances*. Se non vengono usati, questi parametri possono essere impostati **rispettivamente** su NULL e su 0.

Dopo l'inizializzazione della fase hull-shader, è necessario inizializzare anche la fase domain-shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Cenni preliminari sull'a tessellazione](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 





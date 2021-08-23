---
title: Come creare uno hull shader
description: Questo argomento illustra come creare uno hull shader.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa9fe55a11c68e4cbc247f6509c52b6bac1d01b823d48637ee51073437316f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608991"
---
# <a name="how-to-create-a-hull-shader"></a>Procedura: Creare uno hull shader

Uno hull shader è la prima di tre fasi che funzionano insieme per implementare la [tessellazione.](direct3d-11-advanced-stages-tessellation.md) Gli output dello hull shader guidano la fase del tessellatore, nonché la fase domain-shader. Questo argomento illustra come creare uno hull shader.

Uno hull shader trasforma un set di punti di controllo di input (da un vertex shader) in un set di punti di controllo di output. Il numero di punti di input e di output può variare in base al contenuto e al numero a seconda della trasformazione (una trasformazione tipica è una trasformazione di base).

Uno hull shader restituisce anche informazioni costanti sulle patch, ad esempio fattori a tassellamento, per uno shader di dominio e il tessellatore. La fase a tessellatore a funzione fissa usa i fattori a tessellazione e gli altri stati dichiarati in uno hull shader per determinare la quantità di tassellamento.

**Per creare uno hull shader**

1.  Progettare uno hull shader. Vedere [Procedura: Progettare uno hull shader.](direct3d-11-advanced-stages-hull-shader-design.md)
2.  Compilare il codice shader
3.  Creare un oggetto hull-shader [**usando ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Inizializzare la fase della pipeline [**usando ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Uno shader di dominio deve essere associato alla pipeline se è associato uno hull shader. In particolare, non è valido trasmettere direttamente i punti di controllo dello hull shader con lo shader geometry.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Panoramica dell'a tessellazione](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 





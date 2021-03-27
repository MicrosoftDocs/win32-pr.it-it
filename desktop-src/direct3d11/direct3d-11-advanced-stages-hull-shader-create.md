---
title: Come creare uno Hull shader
description: In questo argomento viene illustrato come creare un Hull shader.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708182"
---
# <a name="how-to-create-a-hull-shader"></a>Procedura: creare un Hull shader

Un Hull shader è il primo di tre fasi che interagiscono per implementare lo [schema a mosaico](direct3d-11-advanced-stages-tessellation.md). Gli output dello shader dello scafo rappresentano la fase mosaico, oltre alla fase Domain shader. In questo argomento viene illustrato come creare un Hull shader.

Uno scafo shader trasforma un set di punti di controllo di input (da un vertex shader) in un set di punti di controllo di output. Il numero di punti di input e di output può variare in base al contenuto e al numero a seconda della trasformazione. una trasformazione tipica sarebbe una trasformazione di base.

Un Hull shader restituisce anche informazioni sulle costanti della patch, ad esempio i fattori a mosaico, per uno shader del dominio e il mosaico. La fase mosaico a funzione fissa usa i fattori a mosaico e altri stati dichiarati in uno scafo shader per determinare la quantità di conteggiarla suddividerla.

**Per creare un Hull shader**

1.  Progettare uno scafo dello shader. Vedere [procedura: progettare uno scafo dello shader](direct3d-11-advanced-stages-hull-shader-design.md).
2.  Compilare il codice dello shader
3.  Creare un oggetto Hull shader usando [**ID3D11Device:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Inizializzare la fase della pipeline utilizzando [**sul ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Se è associato un Hull shader, è necessario associare un Domain shader alla pipeline. In particolare, non è consentito trasmettere direttamente i punti di controllo di Hull shader con il geometry shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Panoramica dello schema a mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 





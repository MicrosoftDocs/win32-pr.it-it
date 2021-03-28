---
title: Come creare uno shader di dominio
description: In questo argomento viene illustrato come creare un Domain shader.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044239"
---
# <a name="how-to-create-a-domain-shader"></a>Procedura: creare uno shader di dominio

Un Domain shader è il terzo di tre fasi che interagiscono per implementare lo [schema a mosaico](direct3d-11-advanced-stages-tessellation.md). Gli input per la fase di shader del dominio provengono da uno scafo dello shader. In questo argomento viene illustrato come creare un Domain shader.

Un Domain shader trasforma la geometria della superficie (creata dalla fase mosaico della funzione fissa) usando i punti di controllo di output di Hull shader, i dati della patch di output di Hull shader e un singolo set di coordinate UV di mosaico.

**Per creare un Domain shader**

1.  Progettare un Domain shader. Vedere [procedura: progettare un Domain shader](direct3d-11-advanced-stages-domain-shader-design.md).
2.  Compilare il codice dello shader.
3.  Creare un oggetto di shader di dominio usando [**ID3D11Device:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  Inizializzare la fase della pipeline usando [**sul ID3D11DeviceContext::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
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

 

 





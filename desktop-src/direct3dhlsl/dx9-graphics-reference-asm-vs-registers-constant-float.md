---
title: Registro float costante (HLSL VS Reference)
description: Registro di input vertex shader per una costante a virgola mobile a quattro componenti. Impostare un registro costante con def-vs o SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399174"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>Registro float costante (HLSL VS Reference)

Registro di input vertex shader per una costante a virgola mobile a quattro componenti. Impostare un registro costante con [def-vs](def---vs.md) o [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).

Il file di registro delle costanti è di sola lettura dal punto di vista del vertex shader. Ogni singola istruzione può accedere a un solo registro costante. Tuttavia, ogni origine in tale istruzione può swizzle in modo indipendente e negare il vettore mentre viene letto.

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader. Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader. Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.

Un registro costante viene designato come assoluto o relativo:


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



Il registro costante può essere letto, quindi, usando un indice assoluto o un indice relativo da un registro indirizzi. Le letture dei registri fuori intervallo restituiscono (0,0, 0,0, 0,0, 0,0).

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio che dichiara due costanti a virgola mobile all'interno di uno shader.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Queste costanti vengono caricate ogni volta che viene chiamato [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .

Di seguito è riportato un esempio di utilizzo dell'API.


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



Se si impostano valori costanti con l'API, non è necessaria alcuna dichiarazione dello shader.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro costanti      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 
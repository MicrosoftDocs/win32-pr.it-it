---
title: Registro float costante (informazioni di riferimento su Visual Studio HLSL)
description: Registro di input vertex shader per una costante a virgola mobile a quattro componenti. Impostare un registro costante con def - vs o SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c81cc05a40ebb7ede53fb14c957584f289a14a15045a2b69f557072c6885c9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949931"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>Registro float costante (informazioni di riferimento su Visual Studio HLSL)

Registro di input vertex shader per una costante a virgola mobile a quattro componenti. Impostare un registro costante con [def - o](def---vs.md) [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).

Il file di registro costante è di sola lettura dal punto di vista del vertex shader. Qualsiasi istruzione singola può accedere a un solo registro costante. Tuttavia, ogni origine in tale istruzione può swizzle in modo indipendente e negare tale vettore durante la lettura.

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con defx assegnano valori allo spazio costante dello shader. La durata di una costante dichiarata con defx è limitata solo all'esecuzione di tale shader. Al contrario, le costanti impostate usando le API SetXXXShaderConstantX inizializzano le costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) fino a quando non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con defx o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che viene eseguito lo shader, le costanti vengono usate dallo shader corrente indipendentemente dalla tecnica usata per impostarli.

Un registro costante viene designato come assoluto o relativo:


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



Il registro costante può essere letto, pertanto, usando un indice assoluto o con un indice relativo da un registro indirizzi. Le operazioni di lettura dai registri non in intervallo restituiscono (0.0, 0.0, 0.0, 0.0).

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di dichiarazione di due costanti a virgola mobile all'interno di uno shader.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Queste costanti vengono caricate ogni volta che [**viene chiamato SetVertexShader.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)

Di seguito è riportato un esempio di uso dell'API .


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



Se si impostano valori costanti con l'API, non è necessaria alcuna dichiarazione di shader.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro costanti      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 
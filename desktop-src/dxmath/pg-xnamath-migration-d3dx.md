---
description: D3DXMath è una libreria helper Math per le applicazioni Direct3D.
ms.assetid: 3067d47f-9b1d-2051-fa24-2094418ea272
title: Uso di D3DXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d463129a453a2b319dd72790bd4546dd90f63a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880125"
---
# <a name="working-with-d3dxmath"></a>Uso di D3DXMath

D3DXMath è una libreria helper Math per le applicazioni Direct3D. D3DXMath è di lunga durata, è incluso in D3DX 9 e D3DX 10 e risale anche alle versioni precedenti di DirectX.

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8, quindi è consigliabile eseguire la migrazione a DirectXMath anziché usare D3DXMath.

 

DirectXMath condivide gran parte della stessa funzionalità in D3DXMath e internamente D3DXMath include diverse ottimizzazioni specifiche del processore. La differenza principale è che D3DXMath è ospitato in D3DX9 \* . Dll e D3DX10 \* . Le dll e pochissime funzioni sono inline. La convenzione di chiamata della libreria DirectXMath è SIMD in modo esplicito, mentre D3DXMath deve eseguire le conversioni di caricamento e archiviazione per implementare l'ottimizzazione SIMD.

## <a name="mixing-directxmath-and-d3dxmath"></a>Combinazione di DirectXMath e D3DXMath

D3DX11 non contiene D3DXMath e, in generale, è consigliabile usare invece DirectXMath. Tuttavia, è possibile continuare a collegarsi a D3DX9 e/o D3DX10 nell'applicazione, pertanto è possibile continuare a usare D3DXMath o usare sia D3DXMath che DirectXMath nell'applicazione nello stesso momento.

È in genere sicuro eseguire il cast di un XMVECTOR \* a una funzione che accetta D3DXVECTOR4 \* o per eseguire il cast di un XMMATRIX \* a una funzione che accetta D3DXMATRIX \* . L'inverso è, tuttavia, non generalmente sicuro perché XMVECTOR e XMMATRIX devono essere allineati a 16 byte, mentre D3DXVECTOR4 e D3DXMATRIX non hanno tale requisito. L'impossibilità di rispettare questo requisito può causare eccezioni di allineamento non valide in fase di esecuzione.

È possibile eseguire il cast di un XMVECTOR \* a una funzione che accetta D3DXVECTOR2 \* o D3DXVECTOR3 \* , ma non viceversa. Entrambe le problematiche di allineamento e il fatto che D3DXVECTOR2 e D3DXVECTOR3 siano strutture di dimensioni minori rendono questa operazione non sicura.

> [!Note]  
> D3DX (e pertanto D3DXMath) è considerato Legacy e non è disponibile per le app di Windows Store eseguite in Windows 8 e non è incluso in Windows 8 SDK per le applicazioni desktop.

 

## <a name="using-directxmath-with-direct3d"></a>Uso di DirectXMath con Direct3D

DirectXMath e D3DXMath sono facoltativi quando si utilizza Direct3D. Direct3D 9 ha definito D3DMATRIX e D3DCOLOR come parte dell'API Direct3D per supportare la pipeline della funzione fissa (ora legacy). D3DXMath in D3DX9 estende questi tipi Direct3D 9 con operazioni matematiche comuni di grafica. Per Direct3D 10. x e Direct3D 11, l'API usa solo la pipeline programmabile, quindi non esiste alcuna struttura specifica dell'API per le matrici o i valori dei colori. Quando le API più recenti richiedono un valore di colore, accettano una matrice esplicita di valori float o un buffer generico di dati costanti interpretato dallo shader HLSL. HLSL stesso può supportare i formati matrice row-major o column-major, quindi il layout è interamente attivo (per altre informazioni, vedere HLSL, [ordinamento matrice](../direct3dhlsl/dx-graphics-hlsl-per-component-math.md); se si usano formati matrice colonna-principale negli shader, è necessario trasporre i dati della matrice DirectXMath quando si posizionano le strutture del buffer costante). Sebbene sia facoltativo, le librerie DirectXMath e D3DXMath forniscono entrambe funzionalità comuni relative alla grafica e sono pertanto estremamente utili quando si esegue la programmazione Direct3D.

È possibile eseguire il cast di un XMVECTOR \* a un D3DVECTOR \* o XMMATRIX \* a D3DMATRIX, \* perché Direct3D 9 non prevede l'allineamento per la struttura dei dati in ingresso. È anche possibile eseguire il cast di XMCOLOR a D3DCOLOR. È possibile convertire una rappresentazione a 4 float del colore in XMCOLOR tramite XMStoreColor () per ottenere il valore DWORD a 8:8:8:8 32 bit equivalente a D3DCOLOR.

Quando si lavora con Direct3D 10. x o Direct3D 11, si usano in genere i tipi DirectXMath per compilare una struttura per ognuno dei buffer costanti e, in questi casi, dipende in gran parte dalla capacità di controllare l'allineamento per renderli efficienti o usare \* operazioni XMStore () per convertire i dati XMVECTOR e XMMATRIX nei tipi di dati corretti. Quando si chiamano le API Direct3D 10. x o Direct3D 11 che richiedono \[ una \] matrice di valori di colore float a 4, è possibile eseguire il cast di un XMVECTOR \* o XMFLOAT4 \* contenente i dati di colore.

## <a name="porting-from-d3dxmath"></a>Porting da D3DXMath



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo D3DXMath</th>
<th>Equivalente DirectXMath</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DXFLOAT16</td>
<td><a href="half-data-type.md"><strong>METÀ</strong></a></td>
</tr>
<tr class="even">
<td>D3DXMATRIX</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4"><strong>XMFLOAT4X4</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXMATRIXA16</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> o <a href="/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)"> <strong>XMFLOAT4X4A</strong></a></td>
</tr>
<tr class="even">
<td>D3DXQUATERNION<br/> D3DXPLANE<br/> D3DXCOLOR<br/></td>
<td><a href="xmvector-data-type.md"><strong>XMVECTOR</strong></a> viene usato anziché avere tipi univoci, quindi sarà probabilmente necessario usare un <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"> <strong>XMFLOAT4</strong></a>
<blockquote>
[!Note]<br />
[<strong>D3DXQUATERNION:: operator *</strong>] (.. /Direct3D9/d3dxquaternion-Extensions.MD) chiama la funzione <a href="/windows/desktop/direct3d9/d3dxquaternionmultiply"><strong>D3DXQuaternionMultiply</strong></a> , che moltiplica due quaternioni. Tuttavia, a meno che non si usi in modo esplicito la funzione <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionmultiply"><strong>XMQuaternionMultiply</strong></a> , si ottiene una risposta errata quando si usa <a href="xmvector-operator-mul.md"><strong>XMVECTOR:: operator *</strong></a> su un quaternione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR2</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2"><strong>XMFLOAT2</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR2_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2"><strong>XMHALF2</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR3</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3"><strong>XMFLOAT3</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR4</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"><strong>XMFLOAT4</strong></a>(o se è possibile garantire che i dati siano allineati a 16 byte, <a href="xmvector-data-type.md"><strong>XMVECTOR</strong></a> o <a href="/previous-versions/windows/desktop/legacy/ee419609(v=vs.85)"><strong>XMFLOAT4A</strong></a> )<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR4_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4"><strong>XMHALF4</strong></a></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Non esiste un equivalente diretto a D3DXVECTOR3 \_ 16F in XNAMath.

 



| D3DXMath (macro) | Equivalente DirectXMath                            |
|----------------|---------------------------------------------------|
| D3DX \_ pi       | [XM \_ pi](ovw-xnamath-reference-constants.md)     |
| \_1BYPI D3DX    | [\_1DIVPI XM](ovw-xnamath-reference-constants.md) |
| D3DXToRadian   | [**XMConvertToRadians**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttoradians)  |
| D3DXToDegree   | [**XMConvertToDegrees**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttodegrees)  |



 



| D3DXMath (funzione)                  | Equivalente DirectXMath                                                                                                                                                                                                                           |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXBoxBoundProbe                  | [**BoundingBox:: Intersects (XMVECTOR, XMVECTOR, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))                                                                                                                                                          |
| D3DXComputeBoundingBox             | [**BoundingBox:: CreateFromPoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfrompoints)                                                                                                                                                                          |
| D3DXComputeBoundingSphere          | [**BoundingSphere:: CreateFromPoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfrompoints)                                                                                                                                                                      |
| D3DXSphereBoundProbe               | [**BoundingSphere:: Intersects (XMVECTOR, XMVECTOR, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_float_))                                                                                                                                                    |
| D3DXIntersectTriFunction           | [**TriangleTests:: Intersects**](ovw-xnamath-triangletests.md)                                                                                                                                                                                   |
| D3DXFloat32To16Array               | [**XMConvertFloatToHalfStream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalfstream)                                                                                                                                                                                 |
| D3DXFloat16To32Array               | [**XMConvertHalfToFloatStream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconverthalftofloatstream)                                                                                                                                                                                 |
| D3DXVec2Length                     | [**XMVector2Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector2length) o [ **XMVector2LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthest)                                                                                                                                                   |
| D3DXVec2LengthSq                   | [**XMVector2LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthsq)                                                                                                                                                                                                   |
| D3DXVec2Dot                        | [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot)                                                                                                                                                                                                             |
| D3DXVec2CCW                        | [**XMVector2Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector2cross)                                                                                                                                                                                                         |
| D3DXVec2Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec2Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec2Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec2Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec2Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec2Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) o [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec2Normalize                  | [**XMVector2Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalize) o [ **XMVector2NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalizeest)                                                                                                                                       |
| D3DXVec2Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) o [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec2CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) o [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec2BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) o [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec2Transform                  | [**XMVector2Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transform)                                                                                                                                                                                                 |
| D3DXVec2TransformCoord             | [**XMVector2TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoord)                                                                                                                                                                                       |
| D3DXVec2TransformNormal            | [**XMVector2TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormal)                                                                                                                                                                                     |
| D3DXVec2TransformArray             | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                                                                                                                                                     |
| D3DXVec2TransformCoordArray        | [**XMVector2TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoordstream)                                                                                                                                                                           |
| D3DXVec2TransformNormalArray       | [**XMVector2TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Length                     | [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length) o [ **XMVector3LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthest)                                                                                                                                                   |
| D3DXVec3LengthSq                   | [**XMVector3LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthsq)                                                                                                                                                                                                   |
| D3DXVec3Dot                        | [**XMVector3Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector3dot)                                                                                                                                                                                                             |
| D3DXVec3Cross                      | [**XMVector3Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector3cross)                                                                                                                                                                                                         |
| D3DXVec3Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec3Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec3Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec3Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec3Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec3Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) o [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec3Normalize                  | [**XMVector3Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalize) o [ **XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest)                                                                                                                                       |
| D3DXVec3Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) o [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec3CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) o [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec3BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) o [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec3Transform                  | [**XMVector3Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)                                                                                                                                                                                                 |
| D3DXVec3TransformCoord             | [**XMVector3TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)                                                                                                                                                                                       |
| D3DXVec3TransformNormal            | [**XMVector3TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)                                                                                                                                                                                     |
| D3DXVec3TransformArray             | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                                                                                                                                                     |
| D3DXVec3TransformCoordArray        | [**XMVector3TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)                                                                                                                                                                           |
| D3DXVec3TransformNormalArray       | [**XMVector3TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Project                    | [**XMVector3Project**](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)                                                                                                                                                                                                     |
| D3DXVec3Unproject                  | [**XMVector3Unproject**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)                                                                                                                                                                                                 |
| D3DXVec3ProjectArray               | [**XMVector3ProjectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)                                                                                                                                                                                         |
| D3DXVec3UnprojectArray             | [**XMVector3UnprojectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)                                                                                                                                                                                     |
| D3DXVec4Length                     | [**XMVector4Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector4length) o [ **XMVector4LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthest)                                                                                                                                                   |
| D3DXVec4LengthSq                   | [**XMVector4LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthsq)                                                                                                                                                                                                   |
| D3DXVec4Dot                        | [**XMVector4Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector4dot)                                                                                                                                                                                                             |
| D3DXVec4Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec4Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec4Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec4Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec4Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec4Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) o [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec4Cross                      | [**XMVector4Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector4cross)                                                                                                                                                                                                         |
| D3DXVec4Normalize                  | [**XMVector4Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalize) o [ **XMVector4NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalizeest)                                                                                                                                       |
| D3DXVec4Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) o [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec4CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) o [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec4BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) o [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec4Transform                  | [**XMVector4Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transform)                                                                                                                                                                                                 |
| D3DXVec4TransformArray             | [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)                                                                                                                                                                                     |
| D3DXMatrixIdentity                 | [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)                                                                                                                                                                                                     |
| D3DXMatrixDeterminant              | [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)                                                                                                                                                                                               |
| D3DXMatrixDecompose                | [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)                                                                                                                                                                                                   |
| D3DXMatrixTranspose                | [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)                                                                                                                                                                                                   |
| D3DXMatrixMultiply                 | [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)                                                                                                                                                                                                     |
| D3DXMatrixMultiplyTranspose        | [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)                                                                                                                                                                                   |
| D3DXMatrixInverse                  | [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)                                                                                                                                                                                                       |
| D3DXMatrixScaling                  | [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)                                                                                                                                                                                                       |
| D3DXMatrixTranslation              | [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)                                                                                                                                                                                               |
| D3DXMatrixRotationX                | [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)                                                                                                                                                                                                   |
| D3DXMatrixRotationY                | [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)                                                                                                                                                                                                   |
| D3DXMatrixRotationZ                | [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)                                                                                                                                                                                                   |
| D3DXMatrixRotationAxis             | [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)                                                                                                                                                                                             |
| D3DXMatrixRotationQuaternion       | [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)                                                                                                                                                                                 |
| D3DXMatrixRotationYawPitchRoll     | [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw) (si noti che l'ordine dei parametri è diverso: D3DXMatrixRotationYawPitchRoll accetta l'imbardata, il pitch, il roll, **XMMatrixRotationRollPitchYaw** prende il passo, l'imbardata, il roll)                 |
| D3DXMatrixTransformation           | [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)                                                                                                                                                                                         |
| D3DXMatrixTransformation2D         | [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)                                                                                                                                                                                     |
| D3DXMatrixAffineTransformation     | [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)                                                                                                                                                                             |
| D3DXMatrixAffineTransformation2D   | [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)                                                                                                                                                                         |
| D3DXMatrixLookAtRH                 | [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)                                                                                                                                                                                                     |
| D3DXMatrixLookAtLH                 | [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)                                                                                                                                                                                                     |
| D3DXMatrixPerspectiveRH            | [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveLH            | [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveFovRH         | [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveFovLH         | [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveOffCenterRH   | [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)                                                                                                                                                                         |
| D3DXMatrixPerspectiveOffCenterLH   | [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)                                                                                                                                                                         |
| D3DXMatrixOrthoRH                  | [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)                                                                                                                                                                                         |
| D3DXMatrixOrthoLH                  | [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)                                                                                                                                                                                         |
| D3DXMatrixOrthoOffCenterRH         | [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)                                                                                                                                                                       |
| D3DXMatrixOrthoOffCenterLH         | [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)                                                                                                                                                                       |
| D3DXMatrixShadow                   | [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)                                                                                                                                                                                                         |
| D3DXMatrixReflect                  | [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)                                                                                                                                                                                                       |
| D3DXQuaternionLength               | [**XMQuaternionLength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlength)                                                                                                                                                                                                 |
| D3DXQuaternionLengthSq             | [**XMQuaternionLengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlengthsq)                                                                                                                                                                                             |
| D3DXQuaternionDot                  | [**XMQuaternionDot**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniondot)                                                                                                                                                                                                       |
| D3DXQuaternionIdentity             | [**XMQuaternionIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionidentity)                                                                                                                                                                                             |
| D3DXQuaternionIsIdentity           | [**XMQuaternionIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisidentity)                                                                                                                                                                                         |
| D3DXQuaternionConjugate            | [**XMQuaternionConjugate**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionconjugate)                                                                                                                                                                                           |
| D3DXQuaternionToAxisAngle          | [**XMQuaternionToAxisAngle**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniontoaxisangle)                                                                                                                                                                                       |
| D3DXQuaternionRotationMatrix       | [**XMQuaternionRotationMatrix**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationmatrix)                                                                                                                                                                                 |
| D3DXQuaternionRotationAxis         | [**XMQuaternionRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationaxis)                                                                                                                                                                                     |
| D3DXQuaternionRotationYawPitchRoll | [**XMQuaternionRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyaw) (si noti che l'ordine dei parametri è diverso: D3DXQuaternionRotationYawPitchRoll accetta l'imbardata, il pitch, il roll, **XMQuaternionRotationRollPitchYaw** prende il passo, l'imbardata, il roll) |
| D3DXQuaternionMultiply             | [**XMQuaternionMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionmultiply)                                                                                                                                                                                             |
| D3DXQuaternionNormalize            | [**XMQuaternionNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalize) o [ **XMQuaternionNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalizeest)                                                                                                                           |
| D3DXQuaternionInverse              | [**XMQuaternionInverse**](/windows/win32/api/directxmath/nf-directxmath-xmquaternioninverse)                                                                                                                                                                                               |
| D3DXQuaternionLn                   | [**XMQuaternionLn**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionln)                                                                                                                                                                                                         |
| D3DXQuaternionExp                  | [**XMQuaternionExp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionexp)                                                                                                                                                                                                       |
| D3DXQuaternionSlerp                | [**XMQuaternionSlerp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerp) o [ **XMQuaternionSlerpV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerpv)                                                                                                                                               |
| D3DXQuaternionSquad                | [**XMQuaternionSquad**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquad) o [ **XMQuaternionSquadV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadv)                                                                                                                                               |
| D3DXQuaternionSquadSetup           | [**XMQuaternionSquadSetup**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadsetup)                                                                                                                                                                                         |
| D3DXQuaternionBaryCentric          | [**XMQuaternionBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentric) o [ **XMQuaternionBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentricv)                                                                                                                       |
| D3DXPlaneDot                       | [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)                                                                                                                                                                                                                 |
| D3DXPlaneDotCoord                  | [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)                                                                                                                                                                                                       |
| D3DXPlaneDotNormal                 | [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)                                                                                                                                                                                                     |
| D3DXPlaneScale                     | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXPlaneNormalize                 | [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize) o [ **XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)                                                                                                                                               |
| D3DXPlaneIntersectLine             | [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)                                                                                                                                                                                             |
| D3DXPlaneFromPointNormal           | [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)                                                                                                                                                                                         |
| D3DXPlaneFromPoints                | [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)                                                                                                                                                                                                   |
| D3DXPlaneTransform                 | [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)                                                                                                                                                                                                     |
| D3DXPlaneTransformArray            | [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)                                                                                                                                                                                         |
| D3DXColorNegative                  | [**XMColorNegative**](/windows/win32/api/directxmath/nf-directxmath-xmcolornegative)                                                                                                                                                                                                       |
| D3DXColorAdd                       | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXColorSubtract                  | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXColorScale                     | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXColorModulate                  | [**XMColorModulate**](/windows/win32/api/directxmath/nf-directxmath-xmcolormodulate)                                                                                                                                                                                                       |
| D3DXColorLerp                      | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) o [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXColorAdjustSaturation          | [**XMColorAdjustSaturation**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustsaturation)                                                                                                                                                                                       |
| D3DXColorAdjustContrast            | [**XMColorAdjustContrast**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustcontrast)                                                                                                                                                                                           |
| D3DXFresnelTerm                    | [**XMFresnelTerm**](/windows/win32/api/directxmath/nf-directxmath-xmfresnelterm)                                                                                                                                                                                                           |



 

> [!Note]  
> Le funzioni [armoniche sferiche](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) per DirectXMath sono disponibili separatamente. Nessun DirectXMath equivalente a **ID3DXMatrixStack**.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 

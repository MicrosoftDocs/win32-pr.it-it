---
description: "Funzione D3DXQuaternionSquadSetup (D3DX10Math.h): imposta i punti di controllo per l'interpolazione quadrangolare sferica."
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Funzione D3DXQuaternionSquadSetup (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 94f6c3fbfa72a46132efe0b9a8057983728d161cc06ba0364019f9d39b4635fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990981"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a>Funzione D3DXQuaternionSquadSetup (D3DX10Math.h)

Imposta i punti di controllo per l'interpolazione quadrangolare sferica.

## <a name="syntax"></a>Sintassi


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore ad AOut.

</dd> <dt>

*pBOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a BOut.

</dd> <dt>

*pCOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a COut.

</dd> <dt>

*pQ0* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q0.

</dd> <dt>

*pQ1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q1.

</dd> <dt>

*pQ2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q2.

</dd> <dt>

*pQ3* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q3.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

Questa funzione accetta quattro punti di controllo, forniti agli input pQ0, pQ1, pQ2 e pQ3. La funzione modifica quindi questi valori per trovare una curva che scorre lungo il percorso più breve. I valori di q0, q2 e q3 vengono calcolati come illustrato di seguito.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Dopo aver calcolato i nuovi valori Q, i valori per AOut, BOut e COut vengono calcolati come segue:

AOut = q1 \* e<sup> \[ -0,25\ \* (\ Ln \[ Exp(q1) \* q2 \] \ +\ Ln \[ Exp(q1) \* q0 \ \] )\ \] </sup>

BOut = q2 \* e<sup> \[ -0,25\ \* (\ Ln \[ Exp(q2) \* q3 \] \ +\ Ln \[ Exp(q2) \* q1 \ \] )\ \] </sup>

COut = q2

> [!Note]  
> Ln è il metodo API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) e Exp è il metodo API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).

 

Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

### <a name="examples"></a>Esempio

L'esempio seguente illustra come usare un set di chiavi quaternione (Q0, Q1, Q2, Q3) per calcolare i punti quadrangolare interni (A, B, C). Ciò garantisce che le tangenti siano continue tra segmenti adiacenti.


```
      A     B
Q0    Q1    Q2    Q3
```



L'esempio di codice seguente illustra come è possibile eseguire l'interpolazione tra Q1 e Q2.


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   C è +/- Q2 a seconda del risultato della funzione.
> -   Qt è il risultato della funzione.
>
> Il risultato è una rotazione di 45 gradi intorno all'asse z per il tempo = 0,5.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

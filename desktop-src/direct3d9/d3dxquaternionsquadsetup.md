---
description: Imposta i punti di controllo per l'interpolazione quadrangolare sferica.
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: Funzione D3DXQuaternionSquadSetup (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 04bae9dafbb9df90fdcccee830a1eecb64c1430f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322487"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a>Funzione D3DXQuaternionSquadSetup (D3dx9math. h)

Imposta i punti di controllo per l'interpolazione quadrangolare sferica.

## <a name="syntax"></a>Sintassi


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAOut* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a AOut.

</dd> <dt>

*pBOut* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore all'attacco.

</dd> <dt>

*pCOut* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a COut.

</dd> <dt>

*pQ0* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q0.

</dd> <dt>

*pQ1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q1.

</dd> <dt>

*pQ2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q2.

</dd> <dt>

*pQ3* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore al punto di controllo di input, Q3.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

Questa funzione accetta quattro punti di controllo, che vengono forniti agli input pQ0, pQ1, pQ2 e pQ3. La funzione modifica quindi questi valori per trovare una curva che scorre lungo il percorso più breve. I valori di Q0, Q2 e Q3 vengono calcolati come illustrato di seguito.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Dopo aver calcolato i nuovi valori Q, i valori per AOut, BOut e COut vengono calcolati come segue:

AOut = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q1) \* Q2 \] \ + \ LN \[ Exp (Q1) \* Q0 \] \) \ \] </sup>

BOut = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q2) \* Q3 \] \ + \ LN \[ Exp (Q2) \* Q1 \] \) \ \] </sup>

COut = Q2

> [!Note]  
> Ln è il metodo API [**D3DXQuaternionLn**](d3dxquaternionln.md) e exp è il metodo API [**D3DXQuaternionExp**](d3dxquaternionexp.md).

 

Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

### <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare un set di chiavi Quaternion (q0, Q1, Q2, Q3) per calcolare i punti quadrangolari interni (A, B, C). In questo modo si garantisce che le tangenti siano continue tra i segmenti adiacenti.


```
      A     B
Q0    Q1    Q2    Q3
```



Nell'esempio di codice riportato di seguito viene illustrato come è possibile interpolare tra Q1 e Q2.


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
> -   C è +/-Q2 a seconda del risultato della funzione.
> -   QT è il risultato della funzione.
>
> Il risultato è una rotazione di 45 gradi intorno all'asse z per time = 0,5.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 





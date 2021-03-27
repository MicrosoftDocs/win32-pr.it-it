---
title: Tipo di buffer
description: Utilizzare la sintassi seguente per dichiarare una variabile del buffer.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Tipo di buffer HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046944"
---
# <a name="buffer-type"></a>Tipo di buffer

Utilizzare la sintassi seguente per dichiarare una variabile del buffer.



| Nome del *tipo* di<del buffer >  ; |
|------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**
</dt> <dd>

Parola chiave required.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Uno dei tipi [Scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md)e some [Matrix](dx-graphics-hlsl-matrix.md) HLSL. È possibile dichiarare una variabile di buffer con una matrice purché si trovino in quantità a 4 32 bit. Quindi, è possibile scrivere `Buffer<float2x2>` . Ma `Buffer<float4x4>` è troppo grande e il compilatore genererà un errore.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome della variabile.

</dd> </dl>

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di una dichiarazione di buffer dal file PipesGS. FX nell' [esempio PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



I dati vengono letti da un buffer usando una versione di overload della funzione intrinseca [**Load**](dx-graphics-hlsl-to-load.md) HLSL che accetta un parametro di input (un indice Integer). È possibile accedere a un buffer come una matrice di elementi; Pertanto, in questo esempio viene letto il secondo elemento.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Usare la [fase Stream-output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) per restituire i dati in un buffer.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 
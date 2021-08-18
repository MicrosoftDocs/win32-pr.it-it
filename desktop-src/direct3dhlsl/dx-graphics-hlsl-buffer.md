---
title: Tipo di buffer
description: Usare la sintassi seguente per dichiarare una variabile di buffer.
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
ms.openlocfilehash: 78d0b452a387ed1d4bf750062963996d0248fa249954a99be581118560866123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120345"
---
# <a name="buffer-type"></a>Tipo di buffer

Usare la sintassi seguente per dichiarare una variabile di buffer.



| Nome<*tipo di* >  *buffer*; |
|------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**
</dt> <dd>

Parola chiave obbligatoria.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*digitare*
</dt> <dd>

Uno dei tipi [scalari](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md)e di alcuni [tipi](dx-graphics-hlsl-matrix.md) HLSL della matrice. È possibile dichiarare una variabile di buffer con una matrice purché si adatti a 4 quantità a 32 bit. È quindi possibile scrivere `Buffer<float2x2>` . Ma `Buffer<float4x4>` è troppo grande e il compilatore genererà un errore.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome della variabile.

</dd> </dl>

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di dichiarazione di buffer dal file PipesGS.fx in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



I dati vengono letti da un buffer usando una versione di overload della funzione intrinseca [**Load**](dx-graphics-hlsl-to-load.md) HLSL che accetta un parametro di input (un indice integer). Si accede a un buffer come una matrice di elementi. Pertanto, questo esempio legge il secondo elemento.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Usare la [fase stream-output per](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) eseguire l'output dei dati in un buffer.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 
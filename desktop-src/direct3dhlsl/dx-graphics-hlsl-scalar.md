---
title: Tipi scalari
description: Tipi scalari
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Tipi scalari HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 39097dd358fcf9da1685be517742291ef96332f2307f255274445da70e4fc050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725935"
---
# <a name="scalar-types"></a>Tipi scalari


HLSL supporta diversi tipi di dati scalari:

-   **bool:** true o false.
-   **int** : intero con segno a 32 bit.
-   **uint** : intero senza segno a 32 bit.
-   **dword** : intero senza segno a 32 bit.
-   **half** - valore a virgola mobile a 16 bit. Questo tipo di dati viene fornito solo per la compatibilità del linguaggio. Le destinazioni shader Direct3D 10 e mappano tutti i metà tipi di dati ai tipi di dati float. Non è possibile usare un tipo di dati half in una variabile globale uniforme (usare il flag /Gec se si desidera questa funzionalità).
-   **float** : valore a virgola mobile a 32 bit.
-   **double** : valore a virgola mobile a 64 bit. Non è possibile usare valori a precisione doppia come input e output per un flusso. Per passare valori a precisione doppia tra shader, dichiarare ogni **valore double** come coppia di tipi di **dati uint.** Usare quindi la funzione [**asuint**](asuint.md) per imballare ogni valore **double** nella coppia di **uint** s e la funzione [**asdouble**](asdouble.md) per disimballare la coppia **di uint** s nel **valore double**.

A partire da Windows 8 HLSL supporta anche tipi di dati scalari con precisione minima. I driver di grafica possono implementare tipi di dati scalari con precisione minima usando qualsiasi precisione maggiore o uguale alla precisione in bit specificata. È consigliabile non basarsi su un comportamento di chiusura o ritorno a capo che dipende da una precisione sottostante specifica. Ad esempio, il driver di grafica potrebbe eseguire operazioni aritmetiche su un valore **min16float** con una precisione a 32 bit completa.

-   **min16float:** valore minimo a virgola mobile a 16 bit.
-   **min10float:** valore minimo a virgola mobile a 10 bit.
-   **min16int:** intero con segno a 16 bit minimo.
-   **min12int:** intero con segno a 12 bit minimo.
-   **min16uint:** intero senza segno a 16 bit minimo.

Per altre informazioni sui valori letterali scalari, vedere [Grammatica](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 10 i tipi seguenti sono modificatori del tipo float.<br/>
<ul>
<li><strong>snorm float</strong> - Float con segno normalizzato IEEE a 32 bit nell'intervallo compreso tra -1 e 1 inclusi.</li>
<li><strong>unorm float</strong> - Float senza segno a 32 bit IEEE nell'intervallo compreso tra 0 e 1 inclusi.</li>
</ul>
Ad esempio, di seguito è illustrata una dichiarazione float-variable con segno normalizzato a 4 componenti.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a>Tipo di stringa

HLSL supporta anche un **tipo stringa,** ovvero una stringa ASCII. Non sono presenti operazioni o stati che accettano stringhe, ma gli effetti possono eseguire query su annotazioni e parametri di stringa.

## <a name="example"></a>Esempio

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a>Vedere anche



* [Dichiarazione di tipi scalari](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
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
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103761896"
---
# <a name="scalar-types"></a>Tipi scalari


HLSL supporta diversi tipi di dati scalari:

-   **bool** : true o false.
-   intero con segno **int** a 32 bit.
-   **uint** -Unsigned Integer a 32 bit.
-   **DWORD** -Unsigned Integer a 32 bit.
-   valore a virgola mobile a **metà** 16 bit. Questo tipo di dati viene fornito solo per la compatibilità con le lingue. Le destinazioni Direct3D 10 shader mappano tutti i tipi di dati a metà per i tipi di dati float. Non è possibile usare un tipo di dati Half in una variabile globale uniforme (usare il flag/GEC se si desidera questa funzionalità).
-   **float** : valore a virgola mobile a 32 bit.
-   valore a virgola mobile a 64 bit **doppio** . Non è possibile usare valori a precisione doppia come input e output per un flusso. Per passare valori a precisione doppia tra shader, dichiarare ogni **Double** come coppia di tipi di dati **uint** . Usare quindi la funzione [**asuint**](asuint.md) per comprimere ogni **Double** nella coppia di **uint** s e la funzione [**AsDouble**](asdouble.md) per decomprimere la coppia di **uint** di nuovo nel **valore Double**.

A partire da Windows 8 HLSL supporta anche i tipi di dati scalari con precisione minima. I driver grafici possono implementare tipi di dati scalari con precisione minima usando una precisione maggiore o uguale alla precisione dei bit specificata. Si consiglia di non basarsi sul comportamento di blocco o wrapping che dipende dalla precisione sottostante specifica. Ad esempio, il driver di grafica potrebbe eseguire operazioni aritmetiche su un valore **min16float** a una precisione completa a 32 bit.

-   **min16float** -valore minimo a virgola mobile a 16 bit.
-   **min10float** -valore a virgola mobile a 10 bit minimo.
-   **min16int** -intero con segno a 16 bit minimo.
-   **min12int** -valore intero con segno a 12 bit minimo.
-   **min16uint** -unsigned integer minimo a 16 bit.

Per ulteriori informazioni sui valori letterali scalari, vedere [grammatica](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 10 i tipi seguenti sono modificatori del tipo float.<br/>
<ul>
<li><strong>russare float</strong> - IEEE a 32 bit con segno-float normalizzato nell'intervallo compreso tra 1 e 1.</li>
<li><strong>float unorm</strong> - IEEE a 32 bit senza segno: float normalizzato nell'intervallo compreso tra 0 e 1 inclusi.</li>
</ul>
Ecco ad esempio una dichiarazione con variabile float normalizzata a 4 componenti.<br/> <span data-codelanguage=""></span>
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

HLSL supporta anche un tipo **stringa** , che è una stringa ASCII. Non sono presenti operazioni o Stati che accettano stringhe, ma gli effetti possono eseguire query su parametri e annotazioni di stringa.

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
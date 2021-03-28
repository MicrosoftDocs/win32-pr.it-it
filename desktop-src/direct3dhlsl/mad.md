---
title: mad (funzione)
description: Esegue un'operazione di moltiplicazione/aggiunta aritmetica su tre valori.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- funzione MAD HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104472006"
---
# <a name="mad-function"></a>mad (funzione)

Esegue un'operazione di moltiplicazione/aggiunta aritmetica su tre valori.

## <a name="syntax"></a>Sintassi

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*mvalue* \[ in\]
</dt> <dd>

Tipo: **numerico**

Valore di moltiplicazione.

</dd> <dt>

*avalue* \[ in\]
</dt> <dd>

Tipo: **numerico**

Primo valore di aggiunta.

</dd> <dt>

*bValue* \[ in\]
</dt> <dd>

Tipo: **numerico**

Secondo valore di aggiunta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **numerico**

Risultato di *mvalue* \* *avalue*  +  *bValue*.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Gli autori dello shader possono usare il intrinseche **MAD** per impostare in modo esplicito come destinazione l'istruzione hardware **MAD** nell'output dello shader compilato, che è particolarmente utile con gli shader che contrassegnano i risultati con la parola chiave [precisa](dx-graphics-hlsl-appendix-keywords.md) . L'istruzione **MAD** può essere implementata nell'hardware come "con fusione", che offre una maggiore precisione rispetto all'implementazione di un'istruzione **mul** seguita da un'istruzione **Add** o da un'operazione **mul**  +  **Add**.

Se gli autori dello shader usano il intrinseche **MAD** per calcolare un risultato contrassegnato come preciso dallo shader, indicano all'hardware di usare qualsiasi implementazione valida dell'istruzione **MAD** (fusa o meno), purché l'implementazione sia coerente per tutti gli usi di tale intrinseca intrinseca in qualsiasi shader **su tale hardware** . Gli shader possono quindi sfruttare i vantaggi dei potenziali miglioramenti delle prestazioni usando un'istruzione **MAD** nativa (rispetto a **mul**  +  **Add**) su alcuni componenti hardware. Il risultato dell'esecuzione di un'istruzione hardware **MAD** nativa potrebbe essere diverso rispetto all'esecuzione di un **mul** seguito da un **Add**. Tuttavia, qualunque sia il risultato, il risultato deve essere coerente affinché la stessa operazione venga eseguita in più shader o in parti diverse di uno shader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





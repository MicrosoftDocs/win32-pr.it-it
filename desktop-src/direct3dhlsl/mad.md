---
title: mad (funzione)
description: Esegue un'operazione aritmetica di moltiplicazione/aggiunta su tre valori.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- Funzione mad HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52e0e4819e4c78f092ee99c78403ace5d0205037db3096dfe45865c2216d486d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788821"
---
# <a name="mad-function"></a>mad (funzione)

Esegue un'operazione aritmetica di moltiplicazione/aggiunta su tre valori.

## <a name="syntax"></a>Sintassi

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*mvalue* \[ Pollici\]
</dt> <dd>

Tipo: **numeric**

Valore di moltiplicazione.

</dd> <dt>

*avalue* \[ Pollici\]
</dt> <dd>

Tipo: **numeric**

Primo valore di addizione.

</dd> <dt>

*bvalue* \[ Pollici\]
</dt> <dd>

Tipo: **numeric**

Secondo valore di addizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **numeric**

Risultato di *mvalue* \* *avalue*  +  *bvalue*.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Gli autori di  shader possono usare l'instrinsic di tipo "matto" per impostare in modo esplicito come destinazione l'istruzione **dell'hardware** matto nell'output dello shader compilato, che è particolarmente utile con gli shader che contrassegnano i risultati con la parola chiave [precise.](dx-graphics-hlsl-appendix-keywords.md) **L'istruzione** mad può essere implementata nell'hardware come "fused", che offre  una precisione più elevata rispetto all'implementazione di un'istruzione **mul** seguita da un'istruzione add o come **mul**  +  **add**.

Se gli autori di shader usano l'instrininsic per calcolare un risultato che lo  shader ha contrassegnato come preciso, indicano all'hardware di  usare qualsiasi implementazione valida dell'istruzione "mad" (fusa o meno), purché l'implementazione sia coerente per tutti gli usi di tale intrinseco in qualsiasi shader su tale hardware.  Gli shader possono quindi sfruttare i potenziali miglioramenti delle prestazioni usando un'istruzione nativa di tipo **"mad"** **(anziché mul**  +  **add)** su alcuni componenti hardware. Il risultato dell'esecuzione di **un'istruzione** hardware nativa può essere diverso o meno dall'esecuzione di un **mul** seguito da un elemento **add.** Tuttavia, indipendentemente dal risultato, il risultato deve essere coerente perché la stessa operazione si verifichi in più shader o parti diverse di uno shader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





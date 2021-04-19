---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Riempie un tensore di output con bit generati in modo deterministico, pseudo-casuale e distribuito in modo uniforme. Facoltativamente, questo operatore può anche restituire uno stato del generatore interno aggiornato, che può essere usato durante le esecuzioni successive dell'operatore.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 19e01ec8dc47e65ace996deef5954c35e21bf5bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320264"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>Struttura DML_RANDOM_GENERATOR_OPERATOR_DESC (directml. h)

Riempie un tensore di output con bit generati in modo deterministico, pseudo-casuale e distribuito in modo uniforme. Facoltativamente, questo operatore può anche restituire uno stato del generatore interno aggiornato, che può essere usato durante le esecuzioni successive dell'operatore.

Questo operatore è deterministico e si comporta come se fosse una funzione pura &mdash; , l'esecuzione non produce effetti collaterali e non usa uno stato globale. L'output pseudo-casuale prodotto da questo operatore dipende esclusivamente dai valori specificati in *InputStateTensor*.

I generatori implementati da questo operatore non sono crittograficamente sicuri. Pertanto, questo operatore non deve essere utilizzato per la crittografia, la generazione di chiavi o altre applicazioni che richiedono la generazione di numeri casuali crittograficamente sicure.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a>Members

`InputStateTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di input contenente lo stato interno del generatore. Le dimensioni e il formato di questo tensore di input dipendono dalla [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).

Per **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, questo tensore deve essere di tipo **UInt32** e avere dimensioni `{1,1,1,6}` . I primi valori a 4 32 bit contengono un contatore a incremento progressivo costante a 128 bit. Gli ultimi valori a 2 32 bit contengono il valore della chiave a 64 bit per il generatore.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

Quando si inizializza lo stato di input del generatore per la prima volta, in genere il contatore a 128 bit (i primi valori UINT32 a 4 32 bit) deve essere inizializzato su 0. La chiave può essere scelta arbitrariamente; valori di chiave diversi produrranno sequenze di numeri differenti. Il valore della chiave viene in genere generato utilizzando un valore di *inizializzazione* fornito dall'utente.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output che include i valori pseudo-casuali risultanti. Questo tensore può essere di qualsiasi dimensione.

`OutputStateTensor`

Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output facoltativo che include lo stato del generatore interno aggiornato. Se specificato, questo operatore usa *InputStateTensor* per calcolare uno stato del generatore aggiornato appropriato e scrive il risultato in *OutputStateTensor*. In genere, i chiamanti salvano il risultato e lo forniscono come stato di input in un'esecuzione successiva di questo operatore.

`Type`

Tipo: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Uno dei valori dell'enumerazione [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , che indica il tipo di generatore da usare. Attualmente l'unico valore valido è **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, che genera numeri pseudo-casuali in base all' [algoritmo PHILOX 4x32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).

## <a name="remarks"></a>Commenti
A ogni esecuzione di questo operatore, è necessario incrementare il contatore a 128 bit. Se viene specificato *OutputStateTensor* , questo operatore incrementa il contatore con il valore corretto per conto dell'utente e scrive il risultato in *OutputStateTensor*. La quantità da incrementare dipende dal numero di elementi di output a 32 bit generati e dal tipo del generatore.

Per **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, il contatore a 128 bit deve essere incrementato di `ceil(outputSize / 4)` a ogni esecuzione, dove `outputSize` è il numero di elementi in *OutputTensor*.

Si consideri un esempio in cui il valore del contatore a 128 bit è attualmente `0x48656c6c'6f46726f'6d536561'74746c65` e la dimensione di OutputTensor è `{3,3,20,7219}` . Dopo l'esecuzione di questo operatore una volta, il contatore deve essere incrementato di 324.855 (il numero di elementi di output generati diviso per 4, arrotondato per eccesso), ottenendo il valore del contatore `0x48656c6c'6f46726f'6d536561'746f776e` . Questo valore aggiornato deve quindi essere fornito come input per la successiva esecuzione di questo operatore.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
`InputStateTensor` e `OutputStateTensor` devono avere le stesse *dimensioni*.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Dimensioni | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputStateTensor | Input | {1, 1, 1, 6} | 4 | UINT32 |
| OutputTensor | Output | {D0, D1, D2, D3} | 4 | UINT32 |
| OutputStateTensor | Output facoltativo | {1, 1, 1, 6} | 4 | UINT32 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |
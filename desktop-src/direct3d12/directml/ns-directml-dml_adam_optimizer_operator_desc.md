---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Calcola i pesi aggiornati (parametri) usando le sfumature fornite, in base all'algoritmo Adam **(ada** ptive **M** oment estimation). Questo operatore è un ottimizzatore e viene in genere usato nel passaggio di aggiornamento del peso di un ciclo di training per eseguire la discesa del gradiente.
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803533"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>DML_ADAM_OPTIMIZER_OPERATOR_DESC struttura (directml.h)

Calcola i pesi aggiornati (parametri) usando le sfumature fornite, in base all'algoritmo Adam **(ada** ptive **M** oment estimation). Questo operatore è un ottimizzatore e viene in genere usato nel passaggio di aggiornamento del peso di un ciclo di training per eseguire la discesa del gradiente.

Questo operatore esegue il calcolo seguente:

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

Oltre a calcolare i parametri di peso aggiornati (restituiti in *OutputParametersTensor),* questo operatore restituisce anche le stime aggiornate per il primo e il secondo momento rispettivamente in *OutputFirstMomentTensor* e *OutputSecondMomentTensor.* In genere, è consigliabile archiviare queste stime del primo e del secondo momento e fornirle come input durante il passaggio di training successivo.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a>Members

`InputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i parametri (pesi) a cui applicare questo ottimizzatore. Le stime del gradiente, del primo e del secondo istante, del passaggio di training corrente, nonché degli iperparamemi *LearningRate*, *Beta1* e *Beta2*, vengono usate da questo operatore per eseguire la discesa del gradiente sui valori di peso forniti in questo tensore.

`InputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente la stima del primo istante della sfumatura per ogni valore di peso. Questi valori vengono in genere ottenuti come risultato di una precedente esecuzione di questo operatore, tramite *OutputFirstMomentTensor*.

Quando si applica questo ottimizzatore a un set di pesi per la prima volta (ad esempio, durante il passaggio di training iniziale), i valori di questo tensore devono in genere essere inizializzati su zero. Le esecuzioni successive devono usare i valori restituiti in *OutputFirstMomentTensor*.

Le *dimensioni* *e il tipo di* dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`InputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente la stima del secondo momento della sfumatura per ogni valore di peso. Questi valori vengono in genere ottenuti come risultato di una precedente esecuzione di questo operatore, tramite *OutputSecondMomentTensor*.

Quando si applica questo ottimizzatore a un set di pesi per la prima volta (ad esempio, durante il passaggio di training iniziale), i valori di questo tensore devono in genere essere inizializzati su zero. Le esecuzioni successive devono usare i valori restituiti in *OutputSecondMomentTensor*.

Le *dimensioni* *e il tipo di* dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`GradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Sfumature da applicare ai parametri di input (pesi) per la discesa della sfumatura. Le sfumature vengono in genere ottenute in un passaggio di backpropagation durante il training.

Le *dimensioni* *e il tipo di* dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`TrainingStepTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore scalare contenente un singolo valore integer che rappresenta il conteggio dei passaggi di training corrente. Questo valore insieme a *Beta1* e *Beta2* viene usato per calcolare il decadimento esponenziale dei tensori di stima del primo e del secondo momento.

In genere il valore del passaggio di training inizia da 0 all'inizio del training e viene incrementato di 1 in ogni passaggio di training successivo. Questo operatore non aggiorna il valore del passaggio di training. È consigliabile eseguire questa operazione manualmente, ad esempio usando [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Questo tensore deve essere scalare (ovvero tutte le dimensioni *uguali* a 1) e avere il tipo di dati [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output che contiene i valori del parametro (peso) aggiornati dopo l'applicazione della discesa del gradiente.

Durante l'associazione, questo tensore è autorizzato a creare un alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore. Per altri [dettagli, vedere](#remarks) la sezione Osservazioni.

I *valori di* Sizes e *DataType* di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor.*

`OutputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente stime aggiornate del primo istante. È necessario archiviare i valori di questo tensore e specificarli in *InputFirstMomentTensor durante* il passaggio di training successivo.

Durante l'associazione, questo tensore è autorizzato a creare un alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore. Per altri [dettagli, vedere](#remarks) la sezione Osservazioni.

I *valori di* Sizes e *DataType* di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor.*

`OutputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente stime aggiornate del secondo momento. È consigliabile archiviare i valori di questo tensore e specificarli in *InputSecondMomentTensor* durante il passaggio di training successivo.

Durante l'associazione, questo tensore è autorizzato a creare un alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore. Per altri [dettagli, vedere](#remarks) la sezione Osservazioni.

I *valori di* Sizes e *DataType* di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor.*

`LearningRate`

Tipo: **float**

La velocità di apprendimento, comunemente definita anche dimensione *del passaggio*. La frequenza di apprendimento è un iperparamerio che determina la grandezza dell'aggiornamento del peso lungo il vettore sfumatura in ogni passaggio di training.

`Beta1`

Tipo: **float**

Iperparamenze che rappresenta il tasso di decadimento esponenziale della stima del primo momento della sfumatura. Questo valore deve essere compreso tra 0,0 e 1,0. Il valore 0,9f è tipico.

`Beta2`

Tipo: **float**

Iperparamenze che rappresenta il tasso di decadimento esponenziale della stima del secondo momento della sfumatura. Questo valore deve essere compreso tra 0,0 e 1,0. Il valore 0,999f è tipico.

`Epsilon`

Tipo: **float**

Valore piccolo usato per facilitare la stabilità numerica impedendo la divisione per zero. Per gli input a virgola mobile a 32 bit, i valori tipici includono 1e-8 o `FLT_EPSILON` .

## <a name="remarks"></a>Commenti
Questo operatore supporta l'esecuzione sul posto, vale a dire che ogni tensore di output può creare un alias di un tensore di input idoneo durante l'associazione. Ad esempio, è possibile associare la stessa risorsa per *InputParametersTensor* e *OutputParametersTensor* per ottenere in modo efficace un aggiornamento sul posto dei parametri di input. Tutti i tensori di input di questo operatore, ad eccezione di *TrainingStepTensor,* sono idonei per l'aliasing in questo modo.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *GradientTensor,* *InputFirstMomentTensor,* *InputParametersTensor,* *InputSecondMomentTensor,* *OutputFirstMomentTensor,* *OutputParametersTensor,* *OutputSecondMomentTensor* e *TrainingStepTensor* devono avere lo stesso *Tipo di dati.*
* *GradientTensor,* *InputFirstMomentTensor,* *InputParametersTensor,* *InputSecondMomentTensor,* *OutputFirstMomentTensor,* *OutputParametersTensor* e *OutputSecondMomentTensor* devono avere le stesse *dimensioni.*

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Dimensioni | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | Input | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| InputFirstMomentTensor | Input | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| InputSecondMomentTensor | Input | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| GradientTensor | Input | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| TrainingStepTensor | Input | { 1, 1, 1, 1 } | 4 | FLOAT32, FLOAT16 |
| OutputParametersTensor | Output | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| OutputFirstMomentTensor | Output | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| OutputSecondMomentTensor | Output | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |
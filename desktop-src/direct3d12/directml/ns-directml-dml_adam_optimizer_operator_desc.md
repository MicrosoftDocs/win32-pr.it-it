---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Calcola i pesi aggiornati (parametri) usando le sfumature fornite, in base all'algoritmo Adam (**Ada** ptive **M** oment estimat). Questo operatore è un ottimizzatore e viene in genere usato nel passaggio di aggiornamento del peso di un ciclo di training per eseguire la discesa della sfumatura.
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
ms.openlocfilehash: a4acd26f5174bf6c6ae53f5edfdc28cc6c9b1a3d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320277"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>Struttura DML_ADAM_OPTIMIZER_OPERATOR_DESC (directml. h)

Calcola i pesi aggiornati (parametri) usando le sfumature fornite, in base all'algoritmo Adam (**Ada** ptive **M** oment estimat). Questo operatore è un ottimizzatore e viene in genere usato nel passaggio di aggiornamento del peso di un ciclo di training per eseguire la discesa della sfumatura.

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

Oltre a calcolare i parametri di peso aggiornati (restituiti in *OutputParametersTensor*), questo operatore restituisce anche le stime relative al primo e al secondo momento aggiornate rispettivamente in *OutputFirstMomentTensor* e *OutputSecondMomentTensor*. In genere, è consigliabile archiviare le stime del primo e del secondo momento e fornirle come input durante il passaggio di training successivo.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Un tensore contenente i parametri (pesi) a cui applicare l'utilità di ottimizzazione. La sfumatura, il primo e il secondo momento, le stime, il passaggio di training corrente e gli iperparametri *LearningRate*, *beta1* e *beta2*, vengono usati da questo operatore per eseguire la discesa delle sfumature sui valori di peso forniti in questo tensore.

`InputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore che contiene la stima del primo momento della sfumatura per ogni valore di peso. Questi valori vengono in genere ottenuti come risultato di un'esecuzione precedente di questo operatore, tramite *OutputFirstMomentTensor*.

Quando si applica l'utilità di ottimizzazione a un set di pesi per la prima volta, ad esempio durante il passaggio di training iniziale, i valori di questo tensore devono essere in genere inizializzati su zero. Le esecuzioni successive devono usare i valori restituiti in *OutputFirstMomentTensor*.

Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`InputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore che contiene la stima del secondo momento della sfumatura per ogni valore di peso. Questi valori vengono in genere ottenuti come risultato di un'esecuzione precedente di questo operatore, tramite *OutputSecondMomentTensor*.

Quando si applica l'utilità di ottimizzazione a un set di pesi per la prima volta, ad esempio durante il passaggio di training iniziale, i valori di questo tensore devono essere in genere inizializzati su zero. Le esecuzioni successive devono usare i valori restituiti in *OutputSecondMomentTensor*.

Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`GradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Sfumature da applicare ai parametri di input (pesi) per la discesa della sfumatura. Le sfumature vengono in genere ottenute in un passaggio di propagazione durante il training.

Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`TrainingStepTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore scalare contenente un singolo valore integer che rappresenta il conteggio dei passaggi di training correnti. Questo valore, insieme a *beta1* e *beta2* , viene usato per calcolare il decadimento esponenziale del primo e del secondo momento, stimare i tensori.

In genere il valore del passaggio di training inizia da 0 all'inizio del training e viene incrementato di 1 per ogni passaggio di training successivo. Questo operatore non aggiorna il valore del passaggio di training. è necessario eseguire questa operazione manualmente, ad esempio usando [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Questo tensore deve essere un valore scalare (ovvero tutte le *dimensioni* pari a 1) e avere un tipo di dati [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output che include i valori del parametro aggiornato (peso) dopo l'applicazione della discesa della sfumatura.

Durante l'associazione, questo tensore è autorizzato a eseguire l'alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore. Per ulteriori informazioni, vedere la sezione [osservazioni](#remarks) .

Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`OutputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output contenente stime aggiornate del primo momento. È necessario archiviare i valori di questo tensore e fornirli in *InputFirstMomentTensor* durante il passaggio di training successivo.

Durante l'associazione, questo tensore è autorizzato a eseguire l'alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore. Per ulteriori informazioni, vedere la sezione [osservazioni](#remarks) .

Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`OutputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output contenente stime aggiornate del secondo momento. È necessario archiviare i valori di questo tensore e fornirli in *InputSecondMomentTensor* durante il passaggio di training successivo.

Durante l'associazione, questo tensore è autorizzato a eseguire l'alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore. Per ulteriori informazioni, vedere la sezione [osservazioni](#remarks) .

Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.

`LearningRate`

Tipo: **float**

Velocità di apprendimento, nota anche come *dimensione del passaggio*. La velocità di apprendimento è un iperparametro che determina la grandezza dell'aggiornamento del peso lungo il vettore di sfumatura per ogni passaggio di training.

`Beta1`

Tipo: **float**

Iperparametro che rappresenta il tasso di decadimento esponenziale della stima del primo istante della sfumatura. Questo valore deve essere compreso tra 0,0 e 1,0. Il valore 0.9 f è tipico.

`Beta2`

Tipo: **float**

Iperparametro che rappresenta il tasso di decadimento esponenziale della stima del secondo istante della sfumatura. Questo valore deve essere compreso tra 0,0 e 1,0. Il valore 0,999 f è tipico.

`Epsilon`

Tipo: **float**

Valore ridotto utilizzato per facilitare la stabilità numerica impedendo la divisione per zero. Per gli input a virgola mobile a 32 bit, i valori tipici includono 1e-8 o `FLT_EPSILON` .

## <a name="remarks"></a>Commenti
Questo operatore supporta l'esecuzione sul posto, vale a dire che a ogni tensore di output è consentito l'alias di un tensore di input idoneo durante l'associazione. È ad esempio possibile associare la stessa risorsa sia per *InputParametersTensor* che per *OutputParametersTensor* , in modo da ottenere efficacemente un aggiornamento sul posto dei parametri di input. Tutti i tensori di input di questo operatore, ad eccezione di *TrainingStepTensor*, sono idonei per l'aliasing in questo modo.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* e *TrainingStepTensor* devono avere lo stesso *tipo* di dati.
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* e *OutputSecondMomentTensor* devono avere le stesse *dimensioni*.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Dimensioni | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | Input | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputFirstMomentTensor | Input | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputSecondMomentTensor | Input | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| GradientTensor | Input | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| TrainingStepTensor | Input | {1, 1, 1, 1} | 4 | FLOAT32, FLOAT16 |
| OutputParametersTensor | Output | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputFirstMomentTensor | Output | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputSecondMomentTensor | Output | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |
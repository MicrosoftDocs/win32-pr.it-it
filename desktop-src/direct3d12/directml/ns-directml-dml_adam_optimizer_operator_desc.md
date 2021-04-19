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
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="865a4-104">Struttura DML_ADAM_OPTIMIZER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="865a4-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="865a4-105">Calcola i pesi aggiornati (parametri) usando le sfumature fornite, in base all'algoritmo Adam (**Ada** ptive **M** oment estimat).</span><span class="sxs-lookup"><span data-stu-id="865a4-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="865a4-106">Questo operatore è un ottimizzatore e viene in genere usato nel passaggio di aggiornamento del peso di un ciclo di training per eseguire la discesa della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="865a4-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="865a4-107">Questo operatore esegue il calcolo seguente:</span><span class="sxs-lookup"><span data-stu-id="865a4-107">This operator performs the following computation:</span></span>

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

<span data-ttu-id="865a4-108">Oltre a calcolare i parametri di peso aggiornati (restituiti in *OutputParametersTensor*), questo operatore restituisce anche le stime relative al primo e al secondo momento aggiornate rispettivamente in *OutputFirstMomentTensor* e *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="865a4-109">In genere, è consigliabile archiviare le stime del primo e del secondo momento e fornirle come input durante il passaggio di training successivo.</span><span class="sxs-lookup"><span data-stu-id="865a4-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="865a4-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="865a4-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="865a4-111">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="865a4-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="865a4-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="865a4-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="865a4-113">Members</span><span class="sxs-lookup"><span data-stu-id="865a4-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="865a4-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-115">Un tensore contenente i parametri (pesi) a cui applicare l'utilità di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="865a4-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="865a4-116">La sfumatura, il primo e il secondo momento, le stime, il passaggio di training corrente e gli iperparametri *LearningRate*, *beta1* e *beta2*, vengono usati da questo operatore per eseguire la discesa delle sfumature sui valori di peso forniti in questo tensore.</span><span class="sxs-lookup"><span data-stu-id="865a4-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="865a4-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-118">Tensore che contiene la stima del primo momento della sfumatura per ogni valore di peso.</span><span class="sxs-lookup"><span data-stu-id="865a4-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="865a4-119">Questi valori vengono in genere ottenuti come risultato di un'esecuzione precedente di questo operatore, tramite *OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="865a4-120">Quando si applica l'utilità di ottimizzazione a un set di pesi per la prima volta, ad esempio durante il passaggio di training iniziale, i valori di questo tensore devono essere in genere inizializzati su zero.</span><span class="sxs-lookup"><span data-stu-id="865a4-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="865a4-121">Le esecuzioni successive devono usare i valori restituiti in *OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="865a4-122">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="865a4-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-124">Tensore che contiene la stima del secondo momento della sfumatura per ogni valore di peso.</span><span class="sxs-lookup"><span data-stu-id="865a4-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="865a4-125">Questi valori vengono in genere ottenuti come risultato di un'esecuzione precedente di questo operatore, tramite *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="865a4-126">Quando si applica l'utilità di ottimizzazione a un set di pesi per la prima volta, ad esempio durante il passaggio di training iniziale, i valori di questo tensore devono essere in genere inizializzati su zero.</span><span class="sxs-lookup"><span data-stu-id="865a4-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="865a4-127">Le esecuzioni successive devono usare i valori restituiti in *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="865a4-128">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="865a4-129">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-130">Sfumature da applicare ai parametri di input (pesi) per la discesa della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="865a4-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="865a4-131">Le sfumature vengono in genere ottenute in un passaggio di propagazione durante il training.</span><span class="sxs-lookup"><span data-stu-id="865a4-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="865a4-132">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="865a4-133">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-134">Un tensore scalare contenente un singolo valore integer che rappresenta il conteggio dei passaggi di training correnti.</span><span class="sxs-lookup"><span data-stu-id="865a4-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="865a4-135">Questo valore, insieme a *beta1* e *beta2* , viene usato per calcolare il decadimento esponenziale del primo e del secondo momento, stimare i tensori.</span><span class="sxs-lookup"><span data-stu-id="865a4-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="865a4-136">In genere il valore del passaggio di training inizia da 0 all'inizio del training e viene incrementato di 1 per ogni passaggio di training successivo.</span><span class="sxs-lookup"><span data-stu-id="865a4-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="865a4-137">Questo operatore non aggiorna il valore del passaggio di training. è necessario eseguire questa operazione manualmente, ad esempio usando [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="865a4-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="865a4-138">Questo tensore deve essere un valore scalare (ovvero tutte le *dimensioni* pari a 1) e avere un tipo di dati [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span><span class="sxs-lookup"><span data-stu-id="865a4-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="865a4-139">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-140">Un tensore di output che include i valori del parametro aggiornato (peso) dopo l'applicazione della discesa della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="865a4-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="865a4-141">Durante l'associazione, questo tensore è autorizzato a eseguire l'alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore.</span><span class="sxs-lookup"><span data-stu-id="865a4-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="865a4-142">Per ulteriori informazioni, vedere la sezione [osservazioni](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="865a4-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="865a4-143">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="865a4-144">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-145">Un tensore di output contenente stime aggiornate del primo momento.</span><span class="sxs-lookup"><span data-stu-id="865a4-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="865a4-146">È necessario archiviare i valori di questo tensore e fornirli in *InputFirstMomentTensor* durante il passaggio di training successivo.</span><span class="sxs-lookup"><span data-stu-id="865a4-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="865a4-147">Durante l'associazione, questo tensore è autorizzato a eseguire l'alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore.</span><span class="sxs-lookup"><span data-stu-id="865a4-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="865a4-148">Per ulteriori informazioni, vedere la sezione [osservazioni](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="865a4-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="865a4-149">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="865a4-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="865a4-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="865a4-151">Un tensore di output contenente stime aggiornate del secondo momento.</span><span class="sxs-lookup"><span data-stu-id="865a4-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="865a4-152">È necessario archiviare i valori di questo tensore e fornirli in *InputSecondMomentTensor* durante il passaggio di training successivo.</span><span class="sxs-lookup"><span data-stu-id="865a4-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="865a4-153">Durante l'associazione, questo tensore è autorizzato a eseguire l'alias di un tensore di input idoneo, che può essere usato per eseguire un aggiornamento sul posto di questo tensore.</span><span class="sxs-lookup"><span data-stu-id="865a4-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="865a4-154">Per ulteriori informazioni, vedere la sezione [osservazioni](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="865a4-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="865a4-155">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="865a4-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="865a4-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="865a4-156">Type: **float**</span></span>

<span data-ttu-id="865a4-157">Velocità di apprendimento, nota anche come *dimensione del passaggio*.</span><span class="sxs-lookup"><span data-stu-id="865a4-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="865a4-158">La velocità di apprendimento è un iperparametro che determina la grandezza dell'aggiornamento del peso lungo il vettore di sfumatura per ogni passaggio di training.</span><span class="sxs-lookup"><span data-stu-id="865a4-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="865a4-159">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="865a4-159">Type: **float**</span></span>

<span data-ttu-id="865a4-160">Iperparametro che rappresenta il tasso di decadimento esponenziale della stima del primo istante della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="865a4-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="865a4-161">Questo valore deve essere compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="865a4-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="865a4-162">Il valore 0.9 f è tipico.</span><span class="sxs-lookup"><span data-stu-id="865a4-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="865a4-163">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="865a4-163">Type: **float**</span></span>

<span data-ttu-id="865a4-164">Iperparametro che rappresenta il tasso di decadimento esponenziale della stima del secondo istante della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="865a4-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="865a4-165">Questo valore deve essere compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="865a4-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="865a4-166">Il valore 0,999 f è tipico.</span><span class="sxs-lookup"><span data-stu-id="865a4-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="865a4-167">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="865a4-167">Type: **float**</span></span>

<span data-ttu-id="865a4-168">Valore ridotto utilizzato per facilitare la stabilità numerica impedendo la divisione per zero.</span><span class="sxs-lookup"><span data-stu-id="865a4-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="865a4-169">Per gli input a virgola mobile a 32 bit, i valori tipici includono 1e-8 o `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="865a4-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="865a4-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="865a4-170">Remarks</span></span>
<span data-ttu-id="865a4-171">Questo operatore supporta l'esecuzione sul posto, vale a dire che a ogni tensore di output è consentito l'alias di un tensore di input idoneo durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="865a4-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="865a4-172">È ad esempio possibile associare la stessa risorsa sia per *InputParametersTensor* che per *OutputParametersTensor* , in modo da ottenere efficacemente un aggiornamento sul posto dei parametri di input.</span><span class="sxs-lookup"><span data-stu-id="865a4-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="865a4-173">Tutti i tensori di input di questo operatore, ad eccezione di *TrainingStepTensor*, sono idonei per l'aliasing in questo modo.</span><span class="sxs-lookup"><span data-stu-id="865a4-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="865a4-174">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="865a4-174">Availability</span></span>
<span data-ttu-id="865a4-175">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="865a4-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="865a4-176">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="865a4-176">Tensor constraints</span></span>
* <span data-ttu-id="865a4-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* e *TrainingStepTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="865a4-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="865a4-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* e *OutputSecondMomentTensor* devono avere le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="865a4-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="865a4-179">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="865a4-179">Tensor support</span></span>
| <span data-ttu-id="865a4-180">Tensore</span><span class="sxs-lookup"><span data-stu-id="865a4-180">Tensor</span></span> | <span data-ttu-id="865a4-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="865a4-181">Kind</span></span> | <span data-ttu-id="865a4-182">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="865a4-182">Dimensions</span></span> | <span data-ttu-id="865a4-183">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="865a4-183">Supported dimension counts</span></span> | <span data-ttu-id="865a4-184">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="865a4-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="865a4-185">InputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-185">InputParametersTensor</span></span> | <span data-ttu-id="865a4-186">Input</span><span class="sxs-lookup"><span data-stu-id="865a4-186">Input</span></span> | <span data-ttu-id="865a4-187">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="865a4-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="865a4-188">4</span><span class="sxs-lookup"><span data-stu-id="865a4-188">4</span></span> | <span data-ttu-id="865a4-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="865a4-190">InputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="865a4-191">Input</span><span class="sxs-lookup"><span data-stu-id="865a4-191">Input</span></span> | <span data-ttu-id="865a4-192">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="865a4-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="865a4-193">4</span><span class="sxs-lookup"><span data-stu-id="865a4-193">4</span></span> | <span data-ttu-id="865a4-194">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="865a4-195">InputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="865a4-196">Input</span><span class="sxs-lookup"><span data-stu-id="865a4-196">Input</span></span> | <span data-ttu-id="865a4-197">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="865a4-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="865a4-198">4</span><span class="sxs-lookup"><span data-stu-id="865a4-198">4</span></span> | <span data-ttu-id="865a4-199">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="865a4-200">GradientTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-200">GradientTensor</span></span> | <span data-ttu-id="865a4-201">Input</span><span class="sxs-lookup"><span data-stu-id="865a4-201">Input</span></span> | <span data-ttu-id="865a4-202">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="865a4-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="865a4-203">4</span><span class="sxs-lookup"><span data-stu-id="865a4-203">4</span></span> | <span data-ttu-id="865a4-204">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="865a4-205">TrainingStepTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-205">TrainingStepTensor</span></span> | <span data-ttu-id="865a4-206">Input</span><span class="sxs-lookup"><span data-stu-id="865a4-206">Input</span></span> | <span data-ttu-id="865a4-207">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="865a4-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="865a4-208">4</span><span class="sxs-lookup"><span data-stu-id="865a4-208">4</span></span> | <span data-ttu-id="865a4-209">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="865a4-210">OutputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-210">OutputParametersTensor</span></span> | <span data-ttu-id="865a4-211">Output</span><span class="sxs-lookup"><span data-stu-id="865a4-211">Output</span></span> | <span data-ttu-id="865a4-212">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="865a4-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="865a4-213">4</span><span class="sxs-lookup"><span data-stu-id="865a4-213">4</span></span> | <span data-ttu-id="865a4-214">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="865a4-215">OutputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="865a4-216">Output</span><span class="sxs-lookup"><span data-stu-id="865a4-216">Output</span></span> | <span data-ttu-id="865a4-217">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="865a4-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="865a4-218">4</span><span class="sxs-lookup"><span data-stu-id="865a4-218">4</span></span> | <span data-ttu-id="865a4-219">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="865a4-220">OutputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="865a4-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="865a4-221">Output</span><span class="sxs-lookup"><span data-stu-id="865a4-221">Output</span></span> | <span data-ttu-id="865a4-222">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="865a4-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="865a4-223">4</span><span class="sxs-lookup"><span data-stu-id="865a4-223">4</span></span> | <span data-ttu-id="865a4-224">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="865a4-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="865a4-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="865a4-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="865a4-226">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="865a4-226">**Header**</span></span> | <span data-ttu-id="865a4-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="865a4-227">directml.h</span></span> |
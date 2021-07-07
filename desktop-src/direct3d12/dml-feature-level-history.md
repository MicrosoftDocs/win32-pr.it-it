---
title: Cronologia a livello di funzionalità DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282550"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="19777-103">Cronologia a livello di funzionalità DirectML</span><span class="sxs-lookup"><span data-stu-id="19777-103">DirectML feature level history</span></span>

<span data-ttu-id="19777-104">Per informazioni generali sulla cronologia delle versioni di DirectML, vedere [Cronologia delle versioni di DirectML.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="19777-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_4_0"></a><span data-ttu-id="19777-105">DML_FEATURE_LEVEL_4_0</span><span class="sxs-lookup"><span data-stu-id="19777-105">DML_FEATURE_LEVEL_4_0</span></span>

<span data-ttu-id="19777-106">Introdotto in DirectML versione 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="19777-106">Introduced in DirectML version 1.6.0.</span></span>

<span data-ttu-id="19777-107">Aggiunta del supporto per i tipi di operatore seguenti, documentati in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="19777-107">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="19777-108">Per ogni costante di tipo di operatore, tale argomento fornisce un collegamento alla struttura corrispondente.</span><span class="sxs-lookup"><span data-stu-id="19777-108">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="19777-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span><span class="sxs-lookup"><span data-stu-id="19777-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span></span>
* <span data-ttu-id="19777-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="19777-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span></span>
* <span data-ttu-id="19777-111">**DML_OPERATOR_ROI_ALIGN1**</span><span class="sxs-lookup"><span data-stu-id="19777-111">**DML_OPERATOR_ROI_ALIGN1**</span></span>

<span data-ttu-id="19777-112">Supporto del tipo di dati esteso e del conteggio delle dimensioni per gli operatori seguenti, documentati in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="19777-112">Extended data type and dimension count support for the following operators, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="19777-113">Per informazioni dettagliate sul supporto specifico aggiunto in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), vedere l'argomento relativo alla struttura di ogni operatore.</span><span class="sxs-lookup"><span data-stu-id="19777-113">For details on the specific support added in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), see each operator's structure topic.</span></span>

* <span data-ttu-id="19777-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="19777-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="19777-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="19777-116">**DML_OPERATOR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="19777-116">**DML_OPERATOR_CONVOLUTION**</span></span>
* <span data-ttu-id="19777-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="19777-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="19777-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="19777-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="19777-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="19777-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="19777-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="19777-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="19777-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="19777-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="19777-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="19777-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="19777-123">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="19777-123">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="19777-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="19777-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="19777-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="19777-126">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="19777-126">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="19777-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="19777-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>
* <span data-ttu-id="19777-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="19777-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="19777-129">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="19777-129">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="19777-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="19777-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="19777-131">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="19777-131">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="19777-132">Introdotto in DirectML versione 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="19777-132">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="19777-133">Aggiunta del supporto per i tipi di operatore seguenti, documentati in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="19777-133">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="19777-134">Per ogni costante di tipo di operatore, tale argomento fornisce un collegamento alla struttura corrispondente.</span><span class="sxs-lookup"><span data-stu-id="19777-134">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="19777-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="19777-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="19777-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="19777-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="19777-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="19777-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="19777-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="19777-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="19777-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="19777-141">Il numero massimo di dimensioni supportate per gli operatori seguenti è aumentato da 4 a 8.</span><span class="sxs-lookup"><span data-stu-id="19777-141">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="19777-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="19777-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="19777-143">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="19777-143">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="19777-144">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="19777-144">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="19777-145">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="19777-145">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="19777-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="19777-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="19777-147">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="19777-147">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="19777-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="19777-149">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-149">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="19777-150">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="19777-150">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="19777-151">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="19777-151">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="19777-152">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="19777-152">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="19777-153">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="19777-153">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="19777-154">Introdotto in DirectML versione 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="19777-154">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="19777-155">Aggiunta del supporto per i tipi di operatore seguenti, documentati in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="19777-155">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="19777-156">Per ogni costante di tipo di operatore, tale argomento fornisce un collegamento alla struttura corrispondente.</span><span class="sxs-lookup"><span data-stu-id="19777-156">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="19777-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="19777-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="19777-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="19777-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="19777-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="19777-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="19777-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="19777-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="19777-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="19777-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="19777-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="19777-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="19777-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="19777-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="19777-164">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="19777-164">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="19777-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="19777-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="19777-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="19777-168">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="19777-168">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="19777-169">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="19777-169">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="19777-170">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-170">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="19777-171">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="19777-171">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="19777-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="19777-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="19777-173">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="19777-173">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="19777-174">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="19777-174">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="19777-175">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="19777-175">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="19777-176">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="19777-176">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="19777-177">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="19777-177">Added the following enhancements.</span></span>

* <span data-ttu-id="19777-178">Il numero massimo di dimensioni del tensore è stato aumentato da 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="19777-178">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="19777-179">Vedere [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="19777-179">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="19777-180">Agli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di dati Integer.</span><span class="sxs-lookup"><span data-stu-id="19777-180">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="19777-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="19777-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="19777-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="19777-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="19777-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="19777-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="19777-184">**DML_OPERATOR_REDUCE**, quando **si** usa DML_REDUCE_FUNCTION_ARGMIN o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="19777-184">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="19777-185">Sono stati aggiunti i tipi di dati a 64 bit seguenti e sono supportati dagli operatori select.</span><span class="sxs-lookup"><span data-stu-id="19777-185">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="19777-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="19777-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="19777-187">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="19777-187">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="19777-188">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="19777-188">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="19777-189">Funzionalità deprecata.</span><span class="sxs-lookup"><span data-stu-id="19777-189">Deprecated functionality.</span></span>

* <span data-ttu-id="19777-190">**DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** sono stati deprecati.</span><span class="sxs-lookup"><span data-stu-id="19777-190">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="19777-191">È consigliabile usare gli operatori DML_OPERATOR_ARGMIN **e** **DML_OPERATOR_ARGMAX** al loro posto.</span><span class="sxs-lookup"><span data-stu-id="19777-191">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="19777-192">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="19777-192">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="19777-193">Introdotto in DirectML versione 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="19777-193">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="19777-194">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="19777-194">Added the following APIs.</span></span>

* [<span data-ttu-id="19777-195">Interfaccia IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="19777-195">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="19777-196">Supporto del grafo dell'operatore (vedere [IDMLDevice1::CompileGraph)](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="19777-196">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="19777-197">Aggiunta del supporto per i tipi di operatore seguenti, documentati in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="19777-197">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="19777-198">Per ogni costante di tipo di operatore, tale argomento fornisce un collegamento alla struttura corrispondente.</span><span class="sxs-lookup"><span data-stu-id="19777-198">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="19777-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="19777-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="19777-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="19777-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="19777-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="19777-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="19777-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="19777-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="19777-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="19777-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="19777-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="19777-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="19777-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="19777-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="19777-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="19777-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="19777-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="19777-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="19777-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="19777-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="19777-209">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="19777-209">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="19777-210">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="19777-210">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="19777-211">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="19777-211">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="19777-212">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="19777-212">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="19777-213">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="19777-213">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="19777-214">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="19777-214">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="19777-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="19777-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="19777-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="19777-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="19777-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="19777-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="19777-218">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="19777-218">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="19777-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="19777-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="19777-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="19777-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="19777-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="19777-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="19777-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="19777-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="19777-223">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="19777-223">Added the following enhancements.</span></span>

* <span data-ttu-id="19777-224">Agli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di dati Integer.</span><span class="sxs-lookup"><span data-stu-id="19777-224">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="19777-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="19777-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="19777-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="19777-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="19777-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="19777-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="19777-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="19777-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="19777-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="19777-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="19777-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="19777-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="19777-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="19777-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="19777-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="19777-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="19777-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="19777-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="19777-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="19777-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="19777-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="19777-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="19777-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="19777-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="19777-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="19777-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="19777-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="19777-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="19777-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="19777-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="19777-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="19777-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="19777-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="19777-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="19777-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="19777-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="19777-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="19777-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="19777-244">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="19777-244">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="19777-245">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="19777-245">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="19777-246">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="19777-246">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="19777-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="19777-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="19777-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="19777-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="19777-249">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="19777-249">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="19777-250">**DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="19777-250">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="19777-251">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="19777-251">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="19777-252">**DML_OPERATOR_REDUCE**, quando si usa una delle funzioni di riduzione seguenti.</span><span class="sxs-lookup"><span data-stu-id="19777-252">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="19777-253">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="19777-253">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="19777-254">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="19777-254">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="19777-255">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="19777-255">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="19777-256">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="19777-256">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="19777-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="19777-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="19777-258">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="19777-258">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="19777-259">Restrizioni relative alla forma del tensore **per DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="19777-259">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="19777-260">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="19777-260">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="19777-261">Introdotto in DirectML versione 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="19777-261">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="19777-262">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="19777-262">Added the following APIs.</span></span>
* [<span data-ttu-id="19777-263">Funzione DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="19777-263">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="19777-264">DML_FEATURE_LEVEL enumerazione</span><span class="sxs-lookup"><span data-stu-id="19777-264">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="19777-265">Query a livello di funzionalità (vedere [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="19777-265">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="19777-266">Aggiunta del supporto per i tipi di operatore seguenti, documentati in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="19777-266">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="19777-267">Per ogni costante di tipo di operatore, tale argomento fornisce un collegamento alla struttura corrispondente.</span><span class="sxs-lookup"><span data-stu-id="19777-267">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="19777-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="19777-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="19777-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="19777-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="19777-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="19777-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="19777-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="19777-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="19777-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="19777-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="19777-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="19777-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="19777-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="19777-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="19777-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="19777-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="19777-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="19777-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="19777-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="19777-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="19777-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="19777-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="19777-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="19777-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="19777-280">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="19777-280">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="19777-281">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="19777-281">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="19777-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="19777-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="19777-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="19777-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="19777-284">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="19777-284">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="19777-285">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="19777-285">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="19777-286">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="19777-286">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="19777-287">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="19777-287">Added the following enhancements.</span></span>

* <span data-ttu-id="19777-288">Quando si associa una risorsa di input per l'invio di un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), è ora legale fornire una risorsa [con D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (oltre **a D3D12_HEAP_TYPE_DEFAULT**), purché siano impostate anche le proprietà dell'heap appropriate.</span><span class="sxs-lookup"><span data-stu-id="19777-288">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="19777-289">Vedere [Binding in DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="19777-289">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="19777-290">Gli operatori booleani logici seguenti supportano ora tensori di output **UINT8,** oltre al supporto esistente per **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="19777-290">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="19777-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="19777-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="19777-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="19777-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="19777-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="19777-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="19777-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="19777-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="19777-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="19777-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="19777-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="19777-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="19777-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="19777-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="19777-298">Le funzioni di attivazione 5D supportano ora l'uso di stride sui tensori di input e output.</span><span class="sxs-lookup"><span data-stu-id="19777-298">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="19777-299">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="19777-299">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="19777-300">Livello di funzionalità in cui è stato introdotto DirectML.</span><span class="sxs-lookup"><span data-stu-id="19777-300">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="19777-301">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="19777-301">See also</span></span>

* [<span data-ttu-id="19777-302">Cronologia delle versioni di DirectML</span><span class="sxs-lookup"><span data-stu-id="19777-302">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="19777-303">DML_FEATURE_LEVEL enumerazione</span><span class="sxs-lookup"><span data-stu-id="19777-303">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="19777-304">Funzione DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="19777-304">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="19777-305">DML_FEATURE_QUERY_FEATURE_LEVELS struttura</span><span class="sxs-lookup"><span data-stu-id="19777-305">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)

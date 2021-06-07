---
title: Cronologia a livello di funzionalità DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 1e5d9f8b0532b809bab617655694af68ba530430
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521206"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="fa35e-103">Cronologia a livello di funzionalità DirectML</span><span class="sxs-lookup"><span data-stu-id="fa35e-103">DirectML feature level history</span></span>

<span data-ttu-id="fa35e-104">Per informazioni generali sulla cronologia delle versioni di DirectML, vedere [Cronologia delle versioni di DirectML.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="fa35e-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="fa35e-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="fa35e-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="fa35e-106">Introdotto in DirectML versione 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="fa35e-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="fa35e-107">Aggiunta del supporto per gli operatori [seguenti.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="fa35e-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="fa35e-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="fa35e-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="fa35e-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="fa35e-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="fa35e-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="fa35e-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="fa35e-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="fa35e-114">Il numero massimo di dimensioni supportate per gli operatori seguenti è aumentato da 4 a 8.</span><span class="sxs-lookup"><span data-stu-id="fa35e-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="fa35e-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="fa35e-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="fa35e-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="fa35e-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="fa35e-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="fa35e-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="fa35e-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="fa35e-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="fa35e-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="fa35e-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="fa35e-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="fa35e-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="fa35e-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="fa35e-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="fa35e-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="fa35e-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="fa35e-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="fa35e-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="fa35e-127">Introdotto in DirectML versione 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="fa35e-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="fa35e-128">Aggiunta del supporto per gli operatori [seguenti.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="fa35e-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="fa35e-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="fa35e-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="fa35e-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="fa35e-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="fa35e-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="fa35e-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="fa35e-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="fa35e-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="fa35e-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="fa35e-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="fa35e-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="fa35e-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="fa35e-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="fa35e-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="fa35e-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="fa35e-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="fa35e-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="fa35e-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="fa35e-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="fa35e-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="fa35e-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="fa35e-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="fa35e-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="fa35e-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="fa35e-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="fa35e-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="fa35e-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="fa35e-149">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-149">Added the following enhancements.</span></span>

* <span data-ttu-id="fa35e-150">Il numero massimo di dimensioni del tensore è stato aumentato da 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="fa35e-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="fa35e-151">Vedere [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fa35e-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="fa35e-152">Agli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di dati Integer.</span><span class="sxs-lookup"><span data-stu-id="fa35e-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="fa35e-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="fa35e-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="fa35e-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="fa35e-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="fa35e-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="fa35e-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="fa35e-156">**DML_OPERATOR_REDUCE**, quando **si** usa DML_REDUCE_FUNCTION_ARGMIN o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="fa35e-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="fa35e-157">Sono stati aggiunti i tipi di dati a 64 bit seguenti e sono supportati dagli operatori select.</span><span class="sxs-lookup"><span data-stu-id="fa35e-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="fa35e-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="fa35e-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="fa35e-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="fa35e-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="fa35e-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="fa35e-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="fa35e-161">Funzionalità deprecata.</span><span class="sxs-lookup"><span data-stu-id="fa35e-161">Deprecated functionality.</span></span>

* <span data-ttu-id="fa35e-162">**DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** sono stati deprecati.</span><span class="sxs-lookup"><span data-stu-id="fa35e-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="fa35e-163">È consigliabile usare gli operatori DML_OPERATOR_ARGMIN **e** **DML_OPERATOR_ARGMAX** al loro posto.</span><span class="sxs-lookup"><span data-stu-id="fa35e-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="fa35e-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="fa35e-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="fa35e-165">Introdotto in DirectML versione 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="fa35e-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="fa35e-166">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-166">Added the following APIs.</span></span>

* [<span data-ttu-id="fa35e-167">Interfaccia IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="fa35e-167">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="fa35e-168">Supporto del grafo dell'operatore (vedere [IDMLDevice1::CompileGraph)](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="fa35e-168">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="fa35e-169">Aggiunta del supporto per gli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-169">Added support for the following operators.</span></span>

* <span data-ttu-id="fa35e-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="fa35e-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="fa35e-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="fa35e-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="fa35e-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="fa35e-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="fa35e-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="fa35e-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="fa35e-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="fa35e-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="fa35e-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="fa35e-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="fa35e-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="fa35e-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="fa35e-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="fa35e-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="fa35e-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="fa35e-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="fa35e-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="fa35e-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="fa35e-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="fa35e-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="fa35e-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="fa35e-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="fa35e-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="fa35e-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="fa35e-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="fa35e-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="fa35e-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="fa35e-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="fa35e-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="fa35e-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="fa35e-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="fa35e-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="fa35e-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="fa35e-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="fa35e-194">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-194">Added the following enhancements.</span></span>

* <span data-ttu-id="fa35e-195">Agli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di dati Integer.</span><span class="sxs-lookup"><span data-stu-id="fa35e-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="fa35e-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="fa35e-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="fa35e-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="fa35e-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="fa35e-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="fa35e-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="fa35e-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="fa35e-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="fa35e-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="fa35e-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="fa35e-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="fa35e-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="fa35e-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="fa35e-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="fa35e-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="fa35e-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="fa35e-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="fa35e-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="fa35e-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="fa35e-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="fa35e-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="fa35e-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="fa35e-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="fa35e-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="fa35e-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="fa35e-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="fa35e-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="fa35e-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="fa35e-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="fa35e-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="fa35e-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="fa35e-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="fa35e-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="fa35e-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="fa35e-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="fa35e-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="fa35e-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="fa35e-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="fa35e-221">**DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="fa35e-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="fa35e-223">**DML_OPERATOR_REDUCE**, quando si usa una delle funzioni di riduzione seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="fa35e-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="fa35e-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="fa35e-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="fa35e-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="fa35e-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="fa35e-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="fa35e-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="fa35e-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="fa35e-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="fa35e-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="fa35e-230">Restrizioni relative alla forma del tensore **per DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="fa35e-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="fa35e-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="fa35e-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="fa35e-232">Introdotto in DirectML versione 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="fa35e-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="fa35e-233">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-233">Added the following APIs.</span></span>
* [<span data-ttu-id="fa35e-234">Funzione DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="fa35e-234">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="fa35e-235">DML_FEATURE_LEVEL enumerazione</span><span class="sxs-lookup"><span data-stu-id="fa35e-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="fa35e-236">Query a livello di funzionalità (vedere [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="fa35e-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="fa35e-237">Aggiunta del supporto per gli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-237">Added support for the following operators.</span></span>

* <span data-ttu-id="fa35e-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="fa35e-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="fa35e-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="fa35e-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="fa35e-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="fa35e-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="fa35e-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="fa35e-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="fa35e-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="fa35e-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="fa35e-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="fa35e-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="fa35e-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="fa35e-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="fa35e-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="fa35e-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="fa35e-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="fa35e-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="fa35e-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="fa35e-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="fa35e-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="fa35e-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="fa35e-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="fa35e-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="fa35e-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="fa35e-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="fa35e-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="fa35e-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="fa35e-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="fa35e-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="fa35e-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="fa35e-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="fa35e-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="fa35e-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="fa35e-257">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa35e-257">Added the following enhancements.</span></span>

* <span data-ttu-id="fa35e-258">Quando si associa una risorsa di input per l'invio di un [IDMLOperatorInitializer,](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)è ora legale fornire una risorsa [con D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (oltre **a D3D12_HEAP_TYPE_DEFAULT**), purché siano impostate anche le proprietà dell'heap appropriate.</span><span class="sxs-lookup"><span data-stu-id="fa35e-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="fa35e-259">Vedere [Binding in DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="fa35e-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="fa35e-260">Gli operatori booleani logici seguenti supportano ora tensori di output **UINT8,** oltre al supporto esistente per **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="fa35e-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="fa35e-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="fa35e-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="fa35e-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="fa35e-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="fa35e-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="fa35e-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="fa35e-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="fa35e-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="fa35e-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="fa35e-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="fa35e-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="fa35e-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="fa35e-268">Le funzioni di attivazione 5D supportano ora l'uso di stride sui tensori di input e output.</span><span class="sxs-lookup"><span data-stu-id="fa35e-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="fa35e-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="fa35e-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="fa35e-270">Livello di funzionalità in cui è stato introdotto DirectML.</span><span class="sxs-lookup"><span data-stu-id="fa35e-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa35e-271">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa35e-271">See also</span></span>

* [<span data-ttu-id="fa35e-272">Cronologia delle versioni di DirectML</span><span class="sxs-lookup"><span data-stu-id="fa35e-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="fa35e-273">DML_FEATURE_LEVEL enumerazione</span><span class="sxs-lookup"><span data-stu-id="fa35e-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="fa35e-274">Funzione DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="fa35e-274">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="fa35e-275">DML_FEATURE_QUERY_FEATURE_LEVELS struttura</span><span class="sxs-lookup"><span data-stu-id="fa35e-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)

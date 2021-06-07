---
title: Cronologia a livello di funzionalità DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: fdc489184b3220afd0b8c75738fa1d40de207c8d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387050"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="d2fbf-103">Cronologia a livello di funzionalità DirectML</span><span class="sxs-lookup"><span data-stu-id="d2fbf-103">DirectML feature level history</span></span>

<span data-ttu-id="d2fbf-104">Per informazioni generali sulla cronologia delle versioni di DirectML, vedere [Cronologia delle versioni di DirectML.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d2fbf-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="d2fbf-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="d2fbf-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="d2fbf-106">Introdotto in DirectML versione 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="d2fbf-107">Aggiunta del supporto per gli operatori [seguenti.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="d2fbf-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="d2fbf-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="d2fbf-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="d2fbf-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="d2fbf-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="d2fbf-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="d2fbf-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="d2fbf-114">Il numero massimo di dimensioni supportate per gli operatori seguenti è aumentato da 4 a 8.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="d2fbf-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="d2fbf-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="d2fbf-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="d2fbf-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="d2fbf-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="d2fbf-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="d2fbf-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="d2fbf-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="d2fbf-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="d2fbf-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="d2fbf-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="d2fbf-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="d2fbf-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="d2fbf-127">Introdotta in DirectML versione 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="d2fbf-128">Aggiunta del supporto per gli operatori [seguenti.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="d2fbf-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="d2fbf-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="d2fbf-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="d2fbf-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="d2fbf-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="d2fbf-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="d2fbf-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="d2fbf-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="d2fbf-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="d2fbf-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="d2fbf-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="d2fbf-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="d2fbf-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="d2fbf-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="d2fbf-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="d2fbf-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="d2fbf-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="d2fbf-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="d2fbf-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="d2fbf-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="d2fbf-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="d2fbf-149">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-149">Added the following enhancements.</span></span>

* <span data-ttu-id="d2fbf-150">Il numero massimo di dimensioni tensore è stato aumentato da 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="d2fbf-151">Vedere [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d2fbf-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="d2fbf-152">È stato aggiunto il supporto aggiuntivo per i tipi di dati Integer agli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="d2fbf-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="d2fbf-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="d2fbf-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="d2fbf-156">**DML_OPERATOR_REDUCE**, quando si usa **DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="d2fbf-157">Sono stati aggiunti i tipi di dati a 64 bit seguenti e sono supportati dagli operatori select.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="d2fbf-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="d2fbf-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="d2fbf-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="d2fbf-161">Funzionalità deprecata.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-161">Deprecated functionality.</span></span>

* <span data-ttu-id="d2fbf-162">**DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** sono stati deprecati.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="d2fbf-163">È consigliabile usare gli operatori di DML_OPERATOR_ARGMIN **e** **DML_OPERATOR_ARGMAX** al loro posto.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="d2fbf-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="d2fbf-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="d2fbf-165">Introdotto in DirectML versione 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="d2fbf-166">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-166">Added the following APIs.</span></span>

* [<span data-ttu-id="d2fbf-167">Interfaccia IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="d2fbf-167">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="d2fbf-168">Supporto del grafo dell'operatore [(vedere IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="d2fbf-168">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="d2fbf-169">Aggiunta del supporto per gli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-169">Added support for the following operators.</span></span>

* <span data-ttu-id="d2fbf-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="d2fbf-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="d2fbf-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="d2fbf-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="d2fbf-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="d2fbf-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="d2fbf-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="d2fbf-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="d2fbf-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="d2fbf-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="d2fbf-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="d2fbf-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="d2fbf-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="d2fbf-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="d2fbf-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="d2fbf-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="d2fbf-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="d2fbf-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="d2fbf-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="d2fbf-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="d2fbf-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="d2fbf-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="d2fbf-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="d2fbf-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="d2fbf-194">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-194">Added the following enhancements.</span></span>

* <span data-ttu-id="d2fbf-195">È stato aggiunto il supporto aggiuntivo per i tipi di dati Integer agli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="d2fbf-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="d2fbf-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="d2fbf-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="d2fbf-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="d2fbf-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="d2fbf-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="d2fbf-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="d2fbf-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="d2fbf-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="d2fbf-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="d2fbf-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="d2fbf-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="d2fbf-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="d2fbf-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="d2fbf-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="d2fbf-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="d2fbf-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="d2fbf-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="d2fbf-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="d2fbf-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="d2fbf-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="d2fbf-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="d2fbf-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="d2fbf-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="d2fbf-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="d2fbf-221">**DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="d2fbf-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="d2fbf-223">**DML_OPERATOR_REDUCE**, quando si usa una delle funzioni di riduzione seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="d2fbf-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="d2fbf-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="d2fbf-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="d2fbf-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="d2fbf-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="d2fbf-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="d2fbf-230">Restrizioni relative alla forma del tensore **per DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="d2fbf-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="d2fbf-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="d2fbf-232">Introdotto in DirectML versione 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="d2fbf-233">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-233">Added the following APIs.</span></span>
* [<span data-ttu-id="d2fbf-234">Funzione DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="d2fbf-234">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="d2fbf-235">DML_FEATURE_LEVEL enumerazione</span><span class="sxs-lookup"><span data-stu-id="d2fbf-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="d2fbf-236">Query a livello di funzionalità (vedere [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="d2fbf-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="d2fbf-237">Aggiunta del supporto per gli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-237">Added support for the following operators.</span></span>

* <span data-ttu-id="d2fbf-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="d2fbf-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="d2fbf-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="d2fbf-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="d2fbf-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="d2fbf-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="d2fbf-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="d2fbf-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="d2fbf-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="d2fbf-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="d2fbf-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="d2fbf-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="d2fbf-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="d2fbf-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="d2fbf-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="d2fbf-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="d2fbf-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="d2fbf-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="d2fbf-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="d2fbf-257">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-257">Added the following enhancements.</span></span>

* <span data-ttu-id="d2fbf-258">Quando si associa una risorsa di input per l'invio di un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), è ora legale fornire una risorsa [con D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (oltre **a D3D12_HEAP_TYPE_DEFAULT**), purché siano impostate anche le proprietà dell'heap appropriate.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="d2fbf-259">Vedere [Binding in DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="d2fbf-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="d2fbf-260">Gli operatori booleani logici seguenti supportano ora tensori di output **UINT8,** oltre al supporto esistente per **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="d2fbf-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="d2fbf-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="d2fbf-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="d2fbf-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="d2fbf-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="d2fbf-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="d2fbf-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="d2fbf-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="d2fbf-268">Le funzioni di attivazione 5D supportano ora l'uso di stride sui tensori di input e output.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="d2fbf-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="d2fbf-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="d2fbf-270">Livello di funzionalità in cui è stato introdotto DirectML.</span><span class="sxs-lookup"><span data-stu-id="d2fbf-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2fbf-271">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2fbf-271">See also</span></span>

* [<span data-ttu-id="d2fbf-272">Cronologia delle versioni di DirectML</span><span class="sxs-lookup"><span data-stu-id="d2fbf-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="d2fbf-273">DML_FEATURE_LEVEL enumerazione</span><span class="sxs-lookup"><span data-stu-id="d2fbf-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="d2fbf-274">Funzione DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="d2fbf-274">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="d2fbf-275">DML_FEATURE_QUERY_FEATURE_LEVELS struttura</span><span class="sxs-lookup"><span data-stu-id="d2fbf-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)

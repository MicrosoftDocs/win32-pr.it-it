---
title: Cronologia a livello di funzionalità DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 92f5a004b73d608a3958ae0edfa8c6d6b6a523d6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548914"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="2e5c2-103">Cronologia a livello di funzionalità DirectML</span><span class="sxs-lookup"><span data-stu-id="2e5c2-103">DirectML feature level history</span></span>

<span data-ttu-id="2e5c2-104">Per informazioni generali sulla cronologia delle versioni di DirectML, vedere [cronologia delle versioni di DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="2e5c2-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="2e5c2-105">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="2e5c2-105">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="2e5c2-106">Introdotta in DirectML versione 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-106">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="2e5c2-107">Aggiunta del supporto per gli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-107">Added support for the following operators.</span></span>

* [<span data-ttu-id="2e5c2-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span><span class="sxs-lookup"><span data-stu-id="2e5c2-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="2e5c2-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="2e5c2-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="2e5c2-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="2e5c2-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="2e5c2-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="2e5c2-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="2e5c2-115">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-115">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="2e5c2-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="2e5c2-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="2e5c2-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="2e5c2-119">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-119">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="2e5c2-120">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-120">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="2e5c2-121">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-121">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="2e5c2-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="2e5c2-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="2e5c2-124">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-124">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="2e5c2-125">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-125">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="2e5c2-126">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-126">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="2e5c2-127">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-127">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="2e5c2-128">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-128">Added the following enhancements.</span></span>

* <span data-ttu-id="2e5c2-129">Il numero massimo di dimensioni del tensore è stato aumentato da 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-129">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="2e5c2-130">Vedere [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2e5c2-130">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="2e5c2-131">Per gli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-131">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="2e5c2-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="2e5c2-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="2e5c2-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="2e5c2-135">**DML_OPERATOR_REDUCE** quando si utilizza **DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-135">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="2e5c2-136">Sono stati aggiunti i seguenti tipi di dati a 64 bit e sono supportati dagli operatori Select.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-136">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="2e5c2-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="2e5c2-138">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-138">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="2e5c2-139">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-139">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="2e5c2-140">Funzionalità deprecata.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-140">Deprecated functionality.</span></span>

* <span data-ttu-id="2e5c2-141">**DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** sono stati deprecati.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-141">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="2e5c2-142">È preferibile usare la **DML_OPERATOR_ARGMIN** autonoma e gli operatori di **DML_OPERATOR_ARGMAX** nella propria posizione.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-142">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="2e5c2-143">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="2e5c2-143">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="2e5c2-144">Introdotta in DirectML versione 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-144">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="2e5c2-145">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-145">Added the following APIs.</span></span>

* [<span data-ttu-id="2e5c2-146">Interfaccia IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="2e5c2-146">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="2e5c2-147">Supporto dell'operatore Graph (vedere [IDMLDevice1:: CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="2e5c2-147">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="2e5c2-148">Aggiunta del supporto per gli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-148">Added support for the following operators.</span></span>

* <span data-ttu-id="2e5c2-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="2e5c2-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="2e5c2-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="2e5c2-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="2e5c2-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="2e5c2-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="2e5c2-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="2e5c2-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="2e5c2-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="2e5c2-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="2e5c2-159">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-159">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="2e5c2-160">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-160">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="2e5c2-161">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-161">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="2e5c2-162">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-162">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="2e5c2-163">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-163">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="2e5c2-164">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-164">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="2e5c2-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="2e5c2-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="2e5c2-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="2e5c2-168">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-168">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="2e5c2-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="2e5c2-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="2e5c2-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="2e5c2-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="2e5c2-173">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-173">Added the following enhancements.</span></span>

* <span data-ttu-id="2e5c2-174">Per gli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-174">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="2e5c2-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="2e5c2-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="2e5c2-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="2e5c2-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="2e5c2-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="2e5c2-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="2e5c2-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="2e5c2-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="2e5c2-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="2e5c2-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="2e5c2-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="2e5c2-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="2e5c2-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="2e5c2-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="2e5c2-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="2e5c2-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="2e5c2-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="2e5c2-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="2e5c2-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="2e5c2-194">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-194">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="2e5c2-195">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-195">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="2e5c2-196">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-196">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="2e5c2-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="2e5c2-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="2e5c2-199">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-199">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="2e5c2-200">**DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-200">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="2e5c2-201">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-201">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="2e5c2-202">**DML_OPERATOR_REDUCE** quando si utilizza una delle seguenti funzioni di riduzione.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-202">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="2e5c2-203">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-203">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="2e5c2-204">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-204">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="2e5c2-205">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-205">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="2e5c2-206">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-206">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="2e5c2-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="2e5c2-208">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-208">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="2e5c2-209">Restrizioni di forma tensore rilassate per **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-209">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="2e5c2-210">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="2e5c2-210">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="2e5c2-211">Introdotta in DirectML versione 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-211">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="2e5c2-212">Sono state aggiunte le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-212">Added the following APIs.</span></span>
* [<span data-ttu-id="2e5c2-213">Funzione DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="2e5c2-213">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="2e5c2-214">Enumerazione DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="2e5c2-214">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="2e5c2-215">Query a livello di funzionalità (vedere [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="2e5c2-215">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="2e5c2-216">Aggiunta del supporto per gli operatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-216">Added support for the following operators.</span></span>

* <span data-ttu-id="2e5c2-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="2e5c2-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="2e5c2-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="2e5c2-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="2e5c2-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="2e5c2-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="2e5c2-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="2e5c2-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="2e5c2-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="2e5c2-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="2e5c2-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="2e5c2-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="2e5c2-229">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-229">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="2e5c2-230">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-230">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="2e5c2-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="2e5c2-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="2e5c2-233">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-233">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="2e5c2-234">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-234">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="2e5c2-235">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-235">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="2e5c2-236">Sono stati aggiunti i miglioramenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-236">Added the following enhancements.</span></span>

* <span data-ttu-id="2e5c2-237">Quando si associa una risorsa di input per l'invio di un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), è ora possibile fornire una risorsa con [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (oltre al **D3D12_HEAP_TYPE_DEFAULT**), a condizione che vengano impostate anche le proprietà dell'heap appropriate.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-237">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="2e5c2-238">Vedere [Binding in DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="2e5c2-238">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="2e5c2-239">Gli operatori booleani logici seguenti supportano ora i tensori di output **Uint8** , oltre al supporto esistente per **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-239">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="2e5c2-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="2e5c2-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="2e5c2-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="2e5c2-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="2e5c2-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="2e5c2-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="2e5c2-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="2e5c2-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="2e5c2-247">le funzioni di attivazione 5D supportano ora l'uso di stride nei propri tensori di input e di output.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-247">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="2e5c2-248">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="2e5c2-248">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="2e5c2-249">Livello di funzionalità in cui è stato introdotto DirectML.</span><span class="sxs-lookup"><span data-stu-id="2e5c2-249">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e5c2-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e5c2-250">See also</span></span>

<span data-ttu-id="2e5c2-251">Cronologia delle versioni di [DirectML](./dml-version-history.md) 
 [Enumerazione DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [DMLCreateDevice1 (funzione](./directml/nf-directml-dmlcreatedevice1.md) 
 ) [Struttura DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span><span class="sxs-lookup"><span data-stu-id="2e5c2-251">[DirectML version history](./dml-version-history.md)
[DML_FEATURE_LEVEL enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
[DMLCreateDevice1 function](./directml/nf-directml-dmlcreatedevice1.md)
[DML_FEATURE_QUERY_FEATURE_LEVELS structure](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span></span>
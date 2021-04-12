---
description: Definisce i livelli di campionamento multiplo a scena completa che il dispositivo può applicare.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: Enumerazione D3DMULTISAMPLE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355064"
---
# <a name="d3dmultisample_type-enumeration"></a><span data-ttu-id="cae06-103">\_Enumerazione del tipo D3DMULTISAMPLE</span><span class="sxs-lookup"><span data-stu-id="cae06-103">D3DMULTISAMPLE\_TYPE enumeration</span></span>

<span data-ttu-id="cae06-104">Definisce i livelli di campionamento multiplo a scena completa che il dispositivo può applicare.</span><span class="sxs-lookup"><span data-stu-id="cae06-104">Defines the levels of full-scene multisampling that the device can apply.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cae06-105">Syntax</span></span>


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="cae06-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="cae06-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cae06-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ None**</span><span class="sxs-lookup"><span data-stu-id="cae06-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-108">Non è disponibile alcun livello di campionamento multiplo Full-Scene.</span><span class="sxs-lookup"><span data-stu-id="cae06-108">No level of full-scene multisampling is available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE non \_ mascherabile**</span><span class="sxs-lookup"><span data-stu-id="cae06-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE\_NONMASKABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="cae06-110">Abilita il valore della qualità multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="cae06-110">Enables the multisample quality value.</span></span> <span data-ttu-id="cae06-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="cae06-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**Esempi di D3DMULTISAMPLE \_ 2 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE\_2\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-113">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-113">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**Esempi di D3DMULTISAMPLE \_ 3 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE\_3\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-115">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-115">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**Esempi di D3DMULTISAMPLE \_ 4 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE\_4\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-117">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-117">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**Esempi di D3DMULTISAMPLE \_ 5 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE\_5\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-119">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-119">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**Esempi di D3DMULTISAMPLE \_ 6 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE\_6\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-121">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-121">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**Esempi di D3DMULTISAMPLE \_ 7 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE\_7\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-123">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-123">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**Esempi di D3DMULTISAMPLE \_ 8 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE\_8\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-125">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-125">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**Esempi di D3DMULTISAMPLE \_ 9 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE\_9\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-127">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-127">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**Esempi di D3DMULTISAMPLE \_ 10 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE\_10\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-129">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-129">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**Esempi di D3DMULTISAMPLE \_ 11 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE\_11\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-131">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-131">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE \_ 12 \_ esempi**</span><span class="sxs-lookup"><span data-stu-id="cae06-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE\_12\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-133">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-133">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**Esempi di D3DMULTISAMPLE \_ 13 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE\_13\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-135">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-135">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**Esempi di D3DMULTISAMPLE \_ 14 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE\_14\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-137">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-137">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE \_ 15- \_ esempi**</span><span class="sxs-lookup"><span data-stu-id="cae06-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE\_15\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-139">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-139">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**Esempi di D3DMULTISAMPLE \_ 16 \_**</span><span class="sxs-lookup"><span data-stu-id="cae06-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE\_16\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-141">Livello di multicampionamento full-scene disponibile.</span><span class="sxs-lookup"><span data-stu-id="cae06-141">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="cae06-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cae06-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="cae06-143">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cae06-143">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="cae06-144">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cae06-144">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="cae06-145">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cae06-145">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cae06-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="cae06-146">Remarks</span></span>

<span data-ttu-id="cae06-147">Oltre ad abilitare il campionamento multiplo Full-Scene in [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Time, saranno presenti stati di rendering che attivano e disattivano i vari aspetti a livelli con granularità fine.</span><span class="sxs-lookup"><span data-stu-id="cae06-147">In addition to enabling full-scene multisampling at [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, there will be render states that turn various aspects on and off at fine-grained levels.</span></span>

<span data-ttu-id="cae06-148">Il campionamento multiplo è valido solo in una catena di scambio che viene creata o reimpostata con l' \_ effetto di swapping D3DSWAPEFFECT scarto.</span><span class="sxs-lookup"><span data-stu-id="cae06-148">Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT\_DISCARD swap effect.</span></span>

<span data-ttu-id="cae06-149">Il valore di anti-aliasing multicampionamento può essere impostato con i parametri (o parametri secondari) nei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="cae06-149">The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.</span></span>



| <span data-ttu-id="cae06-150">Metodo</span><span class="sxs-lookup"><span data-stu-id="cae06-150">Method</span></span>                                                                                             | <span data-ttu-id="cae06-151">Parametri</span><span class="sxs-lookup"><span data-stu-id="cae06-151">Parameters</span></span>                         | <span data-ttu-id="cae06-152">Parametri secondari</span><span class="sxs-lookup"><span data-stu-id="cae06-152">Sub-parameters</span></span>                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [<span data-ttu-id="cae06-153">**IDirect3D9:: CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="cae06-153">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | <span data-ttu-id="cae06-154">MultiSampleType e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="cae06-154">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="cae06-155">**IDirect3D9:: CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="cae06-155">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | <span data-ttu-id="cae06-156">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="cae06-156">pPresentationParameters</span></span>            | <span data-ttu-id="cae06-157">MultiSampleType e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="cae06-157">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="cae06-158">**IDirect3DDevice9:: CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="cae06-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | <span data-ttu-id="cae06-159">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="cae06-159">pPresentationParameters</span></span>            | <span data-ttu-id="cae06-160">MultiSampleType e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="cae06-160">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="cae06-161">**IDirect3DDevice9:: CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="cae06-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | <span data-ttu-id="cae06-162">MultiSampleType e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="cae06-162">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="cae06-163">**IDirect3DDevice9:: CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="cae06-163">**IDirect3DDevice9::CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | <span data-ttu-id="cae06-164">MultiSampleType e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="cae06-164">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="cae06-165">**IDirect3DDevice9:: Reset**</span><span class="sxs-lookup"><span data-stu-id="cae06-165">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | <span data-ttu-id="cae06-166">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="cae06-166">pPresentationParameters</span></span>            | <span data-ttu-id="cae06-167">MultiSampleType e pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="cae06-167">MultiSampleType and pQualityLevels</span></span> |



 

<span data-ttu-id="cae06-168">Non è consigliabile passare da un tipo multisample a un altro per aumentare la qualità dell'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="cae06-168">It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.</span></span>

<span data-ttu-id="cae06-169">D3DMULTISAMPLE \_ None consente effetti di swapping diversi dall'eliminazione, dal blocco e così via.</span><span class="sxs-lookup"><span data-stu-id="cae06-169">D3DMULTISAMPLE\_NONE enables swap effects other than discarding, locking, and so on.</span></span>

<span data-ttu-id="cae06-170">Indica se il dispositivo di visualizzazione supporta il multicampionamento mascherabile, ovvero più di un campione per un formato di destinazione di rendering multiplo, più il supporto antialias, o semplicemente un multicampionamento non mascherabile (solo supporto antialias), il driver per il dispositivo fornisce il numero di livelli di qualità per il \_ tipo a più campioni non mascherabili di D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="cae06-170">Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE\_NONMASKABLE multiple-sample type.</span></span> <span data-ttu-id="cae06-171">Per le applicazioni che usano solo il campionamento multiplo per scopi di anti-aliasing è sufficiente eseguire una query per il numero di livelli di qualità di più campioni non mascherabili supportati dal driver.</span><span class="sxs-lookup"><span data-stu-id="cae06-171">Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.</span></span>

<span data-ttu-id="cae06-172">I livelli di qualità supportati dal dispositivo possono essere ottenuti con il parametro pQualityLevels di [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="cae06-172">The quality levels supported by the device can be obtained with the pQualityLevels parameter of [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="cae06-173">I livelli di qualità utilizzati dall'applicazione vengono impostati con il parametro MultiSampleQuality di [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) e [**IDirect3DDevice9:: CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span><span class="sxs-lookup"><span data-stu-id="cae06-173">Quality levels used by the application are set with the MultiSampleQuality parameter of [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) and [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span></span>

<span data-ttu-id="cae06-174">\_Per informazioni sul multicampionamento mascherabile, vedere D3DRS MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="cae06-174">See D3DRS\_MULTISAMPLEMASK for discussion of maskable multisampling.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae06-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cae06-175">Requirements</span></span>



| <span data-ttu-id="cae06-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae06-176">Requirement</span></span> | <span data-ttu-id="cae06-177">Valore</span><span class="sxs-lookup"><span data-stu-id="cae06-177">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cae06-178">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cae06-178">Header</span></span><br/> | <dl> <span data-ttu-id="cae06-179"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae06-179"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae06-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cae06-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae06-181">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="cae06-181">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="cae06-182">**\_Parametri D3DPRESENT**</span><span class="sxs-lookup"><span data-stu-id="cae06-182">**D3DPRESENT\_PARAMETERS**</span></span>](d3dpresent-parameters.md)
</dt> <dt>

[<span data-ttu-id="cae06-183">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="cae06-183">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> </dl>

 

 

---
UID: NF:directml.DMLCreateDevice1
title: Funzione DMLCreateDevice1
description: Crea un dispositivo DirectML per un determinato dispositivo Direct3D 12.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803770"
---
# <a name="dmlcreatedevice1-function-directmlh"></a><span data-ttu-id="de4ec-103">Funzione DMLCreateDevice1 (directml.h)</span><span class="sxs-lookup"><span data-stu-id="de4ec-103">DMLCreateDevice1 function (directml.h)</span></span>

<span data-ttu-id="de4ec-104">Crea un dispositivo DirectML per un determinato dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="de4ec-104">Creates a DirectML device for a given Direct3D 12 device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de4ec-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="de4ec-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="de4ec-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="de4ec-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="de4ec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de4ec-107">Syntax</span></span>

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="de4ec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="de4ec-108">Parameters</span></span>

`d3d12Device`

<span data-ttu-id="de4ec-109">Tipo: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span><span class="sxs-lookup"><span data-stu-id="de4ec-109">Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span></span>

<span data-ttu-id="de4ec-110">Puntatore a un [dispositivo ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) che rappresenta il dispositivo Direct3D 12 su cui creare il dispositivo DirectML.</span><span class="sxs-lookup"><span data-stu-id="de4ec-110">A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over.</span></span> <span data-ttu-id="de4ec-111">DirectML supporta qualsiasi livello di funzionalità D3D e dispositivi Direct3D 12 creati in qualsiasi scheda, incluso WARP.</span><span class="sxs-lookup"><span data-stu-id="de4ec-111">DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP.</span></span> <span data-ttu-id="de4ec-112">Tuttavia, non tutte le funzionalità di DirectML possono essere disponibili a seconda delle funzionalità del dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="de4ec-112">However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device.</span></span> <span data-ttu-id="de4ec-113">Per [altre informazioni, vedere IDMLDevice::CheckFeatureSupport.](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="de4ec-113">See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.</span></span>

<span data-ttu-id="de4ec-114">Se la chiamata a **DMLCreateDevice1** ha esito positivo, il dispositivo DirectML mantiene un riferimento sicuro al dispositivo Direct3D 12 fornito.</span><span class="sxs-lookup"><span data-stu-id="de4ec-114">If the call to **DMLCreateDevice1** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.</span></span>

`flags`

<span data-ttu-id="de4ec-115">Tipo: <b>DML_CREATE_DEVICE_FLAGS</b></span><span class="sxs-lookup"><span data-stu-id="de4ec-115">Type: <b>DML_CREATE_DEVICE_FLAGS</b></span></span>

<span data-ttu-id="de4ec-116">Valore [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) che specifica opzioni aggiuntive di creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de4ec-116">A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.</span></span>

`minimumFeatureLevel`

<span data-ttu-id="de4ec-117">Tipo: <b>DML_FEATURE_LEVEL</b></span><span class="sxs-lookup"><span data-stu-id="de4ec-117">Type: <b>DML_FEATURE_LEVEL</b></span></span>

<span data-ttu-id="de4ec-118">Valore [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) che specifica il supporto minimo del livello di funzionalità richiesto.</span><span class="sxs-lookup"><span data-stu-id="de4ec-118">A [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) value specifying the minimum feature level support required.</span></span>

<span data-ttu-id="de4ec-119">Questo parametro può essere utile per i chiamanti che richiedono una versione specifica di DirectML, ma che possono trovarsi a chiamare una versione precedente di DirectML.</span><span class="sxs-lookup"><span data-stu-id="de4ec-119">This parameter can be useful for callers that require a specific version of DirectML, but who may find themselves calling into an older version of DirectML.</span></span> <span data-ttu-id="de4ec-120">Ciò può verificarsi, ad esempio, quando l'utente esegue l'applicazione in una versione precedente di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="de4ec-120">This can happen, for example, when the user runs your application on an older version of Windows 10.</span></span>

<span data-ttu-id="de4ec-121">Le applicazioni che dipendono in modo esplicito dalle funzionalità introdotte in un determinato livello di funzionalità possono specificarlo come *minimumFeatureLevel.*</span><span class="sxs-lookup"><span data-stu-id="de4ec-121">Applications that explicitly depend on functionality introduced in a particular feature level can specify it as a *minimumFeatureLevel*.</span></span> <span data-ttu-id="de4ec-122">Ciò garantisce che **DMLCreateDevice1** avrà esito positivo  solo se l'implementazione sottostante è in grado almeno di questo livello di funzionalità minimo richiesto.</span><span class="sxs-lookup"><span data-stu-id="de4ec-122">This will guarantee that **DMLCreateDevice1** won't succeed unless the underlying implementation is *at least* as capable as this requested minimum feature level.</span></span>

<span data-ttu-id="de4ec-123">Si noti che poiché  questo parametro specifica un livello di funzionalità minimo, il dispositivo DirectML sottostante può infatti supportare un livello di funzionalità superiore al livello minimo richiesto.</span><span class="sxs-lookup"><span data-stu-id="de4ec-123">Note that as this parameter specifies a *minimum* feature level, the underlying DirectML device may in fact support a higher feature level than the requested minimum.</span></span> <span data-ttu-id="de4ec-124">Al termine della creazione del dispositivo, è possibile eseguire una query su tutti i livelli di funzionalità supportati da questo dispositivo usando [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="de4ec-124">Once device creation succeeds, you can query all of the feature levels supported by this device using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span></span>

`riid`

<span data-ttu-id="de4ec-125">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="de4ec-125">Type: <b>REFIID</b></span></span>

<span data-ttu-id="de4ec-126">Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera restituire nel <i>dispositivo</i>.</span><span class="sxs-lookup"><span data-stu-id="de4ec-126">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>.</span></span> <span data-ttu-id="de4ec-127">Si prevede che sia il GUID di [IDMLDevice.](/windows/win32/api/directml/nn-directml-idmldevice)</span><span class="sxs-lookup"><span data-stu-id="de4ec-127">This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

`ppv`

<span data-ttu-id="de4ec-128">Tipo: \_ COM \_ Outptr opt \_ \_ <b>void\*\*</b></span><span class="sxs-lookup"><span data-stu-id="de4ec-128">Type: \_COM\_Outptr\_opt\_ <b>void\*\*</b></span></span>

<span data-ttu-id="de4ec-129">Puntatore a un blocco di memoria che riceve un puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de4ec-129">A pointer to a memory block that receives a pointer to the device.</span></span> <span data-ttu-id="de4ec-130">Si tratta dell'indirizzo di un puntatore a [un oggetto IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)che rappresenta il dispositivo DirectML creato.</span><span class="sxs-lookup"><span data-stu-id="de4ec-130">This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.</span></span>


## <a name="return-value"></a><span data-ttu-id="de4ec-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de4ec-131">Return value</span></span>

<span data-ttu-id="de4ec-132">Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="de4ec-132">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="de4ec-133">Se la funzione ha esito positivo, restituisce <b>S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="de4ec-133">If the function succeeds, it returns <b>S_OK</b>.</span></span> <span data-ttu-id="de4ec-134">In caso contrario, restituisce un [codice di errore HRESULT.](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="de4ec-134">Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.</span></span>

<span data-ttu-id="de4ec-135">Se questa versione di DirectML non supporta *il valore minimumFeatureLevel* richiesto, questa funzione restituirà DXGI_ERROR_UNSUPPORTED **.**</span><span class="sxs-lookup"><span data-stu-id="de4ec-135">If this version of DirectML doesn't support the *minimumFeatureLevel* requested, then this function will return **DXGI_ERROR_UNSUPPORTED**.</span></span>

<span data-ttu-id="de4ec-136">Per usare i livelli di debug DirectML, è necessario installare la funzionalità degli strumenti di grafica su richiesta.</span><span class="sxs-lookup"><span data-stu-id="de4ec-136">The Graphics Tools Feature on Demand (FOD) must be installed in order to use the DirectML debug layers.</span></span> <span data-ttu-id="de4ec-137">Se il [flag DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) viene specificato nei *flag* e i livelli di debug non sono installati, **DMLCreateDevice1** restituisce **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span><span class="sxs-lookup"><span data-stu-id="de4ec-137">If the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag is specified in *flags* and the debug layers are not installed, then **DMLCreateDevice1** returns **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span></span>

## <a name="remarks"></a><span data-ttu-id="de4ec-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="de4ec-138">Remarks</span></span>

<span data-ttu-id="de4ec-139">È stata introdotta una versione più recente di questa funzione, [DMLCreateDevice1,]()in DirectML versione 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="de4ec-139">A newer version of this function, [DMLCreateDevice1](), was introduced in DirectML version 1.1.0.</span></span> <span data-ttu-id="de4ec-140">**DMLCreateDevice1** equivale a chiamare **DMLCreateDevice1** e a fornire *un valore minimumFeatureLevel* [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span><span class="sxs-lookup"><span data-stu-id="de4ec-140">**DMLCreateDevice1** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span></span>

## <a name="availability"></a><span data-ttu-id="de4ec-141">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="de4ec-141">Availability</span></span>

<span data-ttu-id="de4ec-142">Questa API è stata introdotta in DirectML versione `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="de4ec-142">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4ec-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de4ec-143">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="de4ec-144">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="de4ec-144">**Target Platform**</span></span> | <span data-ttu-id="de4ec-145">Windows</span><span class="sxs-lookup"><span data-stu-id="de4ec-145">Windows</span></span> |
| <span data-ttu-id="de4ec-146">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="de4ec-146">**Header**</span></span> | <span data-ttu-id="de4ec-147">directml.h</span><span class="sxs-lookup"><span data-stu-id="de4ec-147">directml.h</span></span> |
| <span data-ttu-id="de4ec-148">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="de4ec-148">**Library**</span></span> | <span data-ttu-id="de4ec-149">DirectML.lib</span><span class="sxs-lookup"><span data-stu-id="de4ec-149">DirectML.lib</span></span> |
| <span data-ttu-id="de4ec-150">**DLL**</span><span class="sxs-lookup"><span data-stu-id="de4ec-150">**DLL**</span></span> | <span data-ttu-id="de4ec-151">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="de4ec-151">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="de4ec-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de4ec-152">See also</span></span>

* [<span data-ttu-id="de4ec-153">DML_FEATURE_LEVEL enumerazione</span><span class="sxs-lookup"><span data-stu-id="de4ec-153">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="de4ec-154">Cronologia delle versioni di DirectML</span><span class="sxs-lookup"><span data-stu-id="de4ec-154">DirectML version history</span></span>](../dml-version-history.md)
* [<span data-ttu-id="de4ec-155">Cronologia a livello di funzionalità DirectML</span><span class="sxs-lookup"><span data-stu-id="de4ec-155">DirectML feature level history</span></span>](/windows/win32/direct3d12/dml-feature_level-history)    
* [<span data-ttu-id="de4ec-156">Uso del livello di debug DirectML</span><span class="sxs-lookup"><span data-stu-id="de4ec-156">Using the DirectML debug layer</span></span>](../dml-debug-layer.md)
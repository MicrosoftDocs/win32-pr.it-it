---
title: Metodo ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Imposta gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Metodo ProcessDeviceWorkItems Direct3D 11
- Metodo ProcessDeviceWorkItems Direct3D 11, interfaccia ID3DX11ThreadPump
- Interfaccia ID3DX11ThreadPump Direct3D 11, metodo ProcessDeviceWorkItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982226"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="ecf0a-107">ID3DX11ThreadPump::P metodo rocessDeviceWorkItems</span><span class="sxs-lookup"><span data-stu-id="ecf0a-107">ID3DX11ThreadPump::ProcessDeviceWorkItems method</span></span>

> [!Note]  
> <span data-ttu-id="ecf0a-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="ecf0a-109">Imposta gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-109">Sets work items to the device after they have finished loading and processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf0a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecf0a-110">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="ecf0a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecf0a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf0a-112">*iWorkItemCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecf0a-112">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf0a-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ecf0a-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ecf0a-114">Numero di elementi di lavoro da impostare sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-114">The number of work items to set to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf0a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecf0a-115">Return value</span></span>

<span data-ttu-id="ecf0a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ecf0a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ecf0a-117">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ecf0a-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf0a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecf0a-118">Remarks</span></span>

<span data-ttu-id="ecf0a-119">Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread Pump lo manterrà in una coda fino a quando non viene chiamata l'API, a quel punto gli elementi elaborati verranno impostati sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-119">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="ecf0a-120">Questa operazione è utile per controllare la quantità di elaborazione dedicata al binding delle risorse al dispositivo per ogni frame.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-120">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span>

<span data-ttu-id="ecf0a-121">Come esempio di come è possibile usare questa API, è possibile che si stia avvicinando alla fine di un livello del gioco e si voglia iniziare a precaricare le trame, gli shader e altre risorse per il livello successivo.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-121">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="ecf0a-122">Il pump di thread inizierà a caricare, decomprimere ed elaborare le risorse e gli shader in un thread separato fino a quando non saranno pronti per essere impostati sul dispositivo, a quel punto li lascerà in una coda.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-122">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="ecf0a-123">È possibile che non si desideri impostare contemporaneamente tutte le risorse e gli shader per il dispositivo, perché ciò può causare un rallentamento temporaneo evidente nelle prestazioni del gioco.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-123">One may not want to set all the resources and shaders to the device at once because this may cause a noticeable temporary slow down in the game's performance.</span></span> <span data-ttu-id="ecf0a-124">Questa API potrebbe quindi essere chiamata una volta per ogni fotogramma, in modo che solo un numero ridotto di elementi di lavoro venga impostato sul dispositivo in ogni frame, distribuendo in tal modo il carico di lavoro delle risorse di associazione al dispositivo su diversi frame.</span><span class="sxs-lookup"><span data-stu-id="ecf0a-124">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf0a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecf0a-125">Requirements</span></span>



| <span data-ttu-id="ecf0a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecf0a-126">Requirement</span></span> | <span data-ttu-id="ecf0a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ecf0a-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf0a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecf0a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ecf0a-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf0a-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="ecf0a-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ecf0a-130">Library</span></span><br/> | <dl> <span data-ttu-id="ecf0a-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecf0a-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ecf0a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecf0a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf0a-133">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="ecf0a-133">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="ecf0a-134">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ecf0a-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 


---
description: Impostare gli elementi di lavoro sul dispositivo dopo aver completato il caricamento e l'elaborazione.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: Metodo ID3DX10ThreadPump::P rocessDeviceWorkItems (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132415"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="12a11-103">ID3DX10ThreadPump::P metodo rocessDeviceWorkItems</span><span class="sxs-lookup"><span data-stu-id="12a11-103">ID3DX10ThreadPump::ProcessDeviceWorkItems method</span></span>

<span data-ttu-id="12a11-104">Impostare gli elementi di lavoro sul dispositivo dopo aver completato il caricamento e l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="12a11-104">Set work items to the device after they have finished loading and processing.</span></span> <span data-ttu-id="12a11-105">Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread Pump lo manterrà in una coda fino a quando non viene chiamata l'API, a quel punto gli elementi elaborati verranno impostati sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12a11-105">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="12a11-106">Questa operazione è utile per controllare la quantità di elaborazione dedicata al binding delle risorse al dispositivo per ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12a11-106">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span> <span data-ttu-id="12a11-107">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="12a11-107">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a11-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12a11-108">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="12a11-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="12a11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a11-110">*iWorkItemCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12a11-110">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a11-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12a11-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12a11-112">Numero di elementi di lavoro da impostare sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12a11-112">The number of work items to set to the device.</span></span> <span data-ttu-id="12a11-113">ProcessDeviceObjectCreation creerà al massimo oggetti iWorkItemCount.</span><span class="sxs-lookup"><span data-stu-id="12a11-113">ProcessDeviceObjectCreation will create at most iWorkItemCount objects.</span></span> <span data-ttu-id="12a11-114">Se nella coda non sono presenti elementi di lavoro sufficienti per elaborare gli oggetti iWorkItemCount, ProcessDeviceObjectCreation creerà un numero di oggetti dispositivo pari a quello degli elementi della coda.</span><span class="sxs-lookup"><span data-stu-id="12a11-114">If there are not enough work items in the queue to process iWorkItemCount objects, ProcessDeviceObjectCreation will create as many device objects as there are items in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12a11-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12a11-115">Return value</span></span>

<span data-ttu-id="12a11-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12a11-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12a11-117">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="12a11-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12a11-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="12a11-118">Remarks</span></span>

<span data-ttu-id="12a11-119">Come esempio di come è possibile usare questa API, è possibile che si stia avvicinando alla fine di un livello del gioco e si voglia iniziare a precaricare le trame, gli shader e altre risorse per il livello successivo.</span><span class="sxs-lookup"><span data-stu-id="12a11-119">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="12a11-120">Il pump di thread inizierà a caricare, decomprimere ed elaborare le risorse e gli shader in un thread separato fino a quando non saranno pronti per essere impostati sul dispositivo, a quel punto li lascerà in una coda.</span><span class="sxs-lookup"><span data-stu-id="12a11-120">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="12a11-121">È possibile che non si desideri impostare contemporaneamente tutte le risorse e gli shader per il dispositivo, perché ciò può causare un rallentamento momentaneo evidente nelle prestazioni del gioco.</span><span class="sxs-lookup"><span data-stu-id="12a11-121">One may not want to set all the resources and shaders to the device at once because this may cause a noticable temporary slow down in the game's performance.</span></span> <span data-ttu-id="12a11-122">Questa API potrebbe quindi essere chiamata una volta per ogni fotogramma, in modo che solo un numero ridotto di elementi di lavoro venga impostato sul dispositivo in ogni frame, in modo da distribuire il carico di lavoro delle risorse di associazione al dispositivo su diversi frame e ridurre al minimo la possibilità di un rallentamento evidente nelle prestazioni del gioco.</span><span class="sxs-lookup"><span data-stu-id="12a11-122">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames and minimizing the possibility of a noticable slow down in the game's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="12a11-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12a11-123">Requirements</span></span>



| <span data-ttu-id="12a11-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="12a11-124">Requirement</span></span> | <span data-ttu-id="12a11-125">Valore</span><span class="sxs-lookup"><span data-stu-id="12a11-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12a11-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12a11-126">Header</span></span><br/>  | <dl> <span data-ttu-id="12a11-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a11-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="12a11-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="12a11-128">Library</span></span><br/> | <dl> <span data-ttu-id="12a11-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12a11-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a11-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12a11-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a11-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="12a11-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="12a11-132">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="12a11-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

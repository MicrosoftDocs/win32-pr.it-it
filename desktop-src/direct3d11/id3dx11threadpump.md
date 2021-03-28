---
title: Interfaccia ID3DX11ThreadPump (D3DX11core. h)
description: Una pompa di thread esegue le attività in modo asincrono.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interfaccia ID3DX11ThreadPump Direct3D 11
- Interfaccia ID3DX11ThreadPump Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119175"
---
# <a name="id3dx11threadpump-interface"></a><span data-ttu-id="1fe1d-105">Interfaccia ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="1fe1d-105">ID3DX11ThreadPump interface</span></span>

> [!Note]  
> <span data-ttu-id="1fe1d-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="1fe1d-107">Una pompa di thread esegue le attività in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-107">A thread pump executes tasks asynchronously.</span></span> <span data-ttu-id="1fe1d-108">Viene creato chiamando [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-108">It is created by calling [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span></span> <span data-ttu-id="1fe1d-109">Sono disponibili diverse API che accettano un thread Pump facoltativo come parametro, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Se si passa un'interfaccia di thread Pump a queste API, le funzioni vengono eseguite in modo asincrono in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-109">There are several APIs that take an optional thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); if you pass a thread pump interface into these APIs, the functions will execute asynchronously on a separate thread.</span></span> <span data-ttu-id="1fe1d-110">In particolare sui computer multiprocessore, una pompa di thread può caricare le risorse ed elaborare i dati senza una riduzione notevole delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-110">Particularly on multiprocessor machines, a thread pump can load resources and process data without a noticeable decrease in performance.</span></span>

## <a name="members"></a><span data-ttu-id="1fe1d-111">Membri</span><span class="sxs-lookup"><span data-stu-id="1fe1d-111">Members</span></span>

<span data-ttu-id="1fe1d-112">L'interfaccia **ID3DX11ThreadPump** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1fe1d-112">The **ID3DX11ThreadPump** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1fe1d-113">**ID3DX11ThreadPump** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-113">**ID3DX11ThreadPump** also has these types of members:</span></span>

-   [<span data-ttu-id="1fe1d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="1fe1d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1fe1d-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="1fe1d-115">Methods</span></span>

<span data-ttu-id="1fe1d-116">L'interfaccia **ID3DX11ThreadPump** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-116">The **ID3DX11ThreadPump** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1fe1d-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="1fe1d-117">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1fe1d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fe1d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1fe1d-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fe1d-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="1fe1d-120">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-120">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fe1d-121">Aggiunge un elemento di lavoro alla pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-121">Adds a work item to the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1fe1d-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fe1d-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="1fe1d-123">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fe1d-124">Ottiene il numero di elementi in ognuna delle tre code all'interno della pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-124">Gets the number of items in each of the three queues inside the thread pump.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1fe1d-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fe1d-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="1fe1d-126">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-126">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fe1d-127">Ottiene il numero di elementi di lavoro nella pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-127">Gets the number of work items in the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1fe1d-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fe1d-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="1fe1d-129">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-129">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fe1d-130">Imposta gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-130">Sets work items to the device after they have finished loading and processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1fe1d-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fe1d-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="1fe1d-132">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fe1d-133">Cancella tutti gli elementi di lavoro dalla pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-133">Clears all work items from the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1fe1d-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fe1d-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="1fe1d-135">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-135">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fe1d-136">Attende il completamento di tutti gli elementi di lavoro nella pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-136">Waits for all work items in the thread pump to finish.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1fe1d-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fe1d-137">Remarks</span></span>

### <a name="using-a-thread-pump"></a><span data-ttu-id="1fe1d-138">Utilizzo di una pompa di thread</span><span class="sxs-lookup"><span data-stu-id="1fe1d-138">Using a Thread Pump</span></span>

<span data-ttu-id="1fe1d-139">Il pump di thread carica ed elabora i dati usando il processo in tre passaggi seguente:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-139">The thread pump loads and processes data using the following three-step process:</span></span>

1.  <span data-ttu-id="1fe1d-140">Caricare e decomprimere i dati con un [**caricatore di dati**](id3dx11dataloader.md).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-140">Load and decompress the data with a [**Data Loader**](id3dx11dataloader.md).</span></span> <span data-ttu-id="1fe1d-141">L'oggetto caricatore di dati dispone di tre metodi che la pompa di thread chiamerà internamente durante il caricamento e la decompressione dei dati: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D eComPress**](id3dx11dataloader-decompress.md)e [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-141">The data loader object has three methods that the thread pump will call internally as it is loading and decompressing the data: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::Decompress**](id3dx11dataloader-decompress.md), and [**ID3DX11DataLoader::Destroy**](id3dx11dataloader-destroy.md).</span></span> <span data-ttu-id="1fe1d-142">Le funzionalità specifiche di queste tre API variano a seconda del tipo di dati caricati e decompressi.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-142">The specific functionality of these three APIs differs depending on the type of data being loaded and decompressed.</span></span> <span data-ttu-id="1fe1d-143">L'interfaccia del caricatore dati può anche essere ereditata e le relative API possono essere modificate se si carica un file di dati definito in un formato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-143">The data loader interface can also be inherited and its APIs can be changed if one is loading a data file defined in one's own custom format.</span></span>
2.  <span data-ttu-id="1fe1d-144">Elaborare i dati con un [**elaboratore di dati**](id3dx11dataprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-144">Process the data with a [**Data Processor**](id3dx11dataprocessor.md).</span></span> <span data-ttu-id="1fe1d-145">L'oggetto elaboratore di dati dispone di tre metodi che la pompa di thread chiamerà internamente durante l'elaborazione dei dati: [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)e [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-145">The data processor object has three methods that the thread pump will call internally as it is processing the data: [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md), and [**ID3DX11DataProcessor::Destroy**](id3dx11dataprocessor-destroy.md).</span></span> <span data-ttu-id="1fe1d-146">La modalità di elaborazione dei dati sarà diversa a seconda del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-146">The way it processes the data will be different depending on the type of data.</span></span> <span data-ttu-id="1fe1d-147">Se, ad esempio, i dati sono una trama archiviata come JPEG, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) eseguirà la decompressione JPEG per ottenere i bit dell'immagine non elaborata dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-147">For example, if the data is a texture stored as a JPEG, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will do JPEG decompression to get the image's raw image bits.</span></span> <span data-ttu-id="1fe1d-148">Se i dati sono uno shader, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) compilerà il HLSL in bytecode.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-148">If the data is a shader, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will compile the HLSL into bytecode.</span></span> <span data-ttu-id="1fe1d-149">Dopo che i dati sono stati elaborati, viene creato un oggetto dispositivo per quei dati (con [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) e l'oggetto verrà aggiunto a una coda di oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-149">After the data has been processed a device object will be created for that data (with [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) and the object will be added to a queue of device objects.</span></span> <span data-ttu-id="1fe1d-150">L'interfaccia del processore dati può anche essere ereditata e le relative API possono essere modificate se si sta elaborando un file di dati definito in un formato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-150">The data processor interface can also be inherited and its APIs can be changed if one is processing a data file defined in one's own custom format.</span></span>
3.  <span data-ttu-id="1fe1d-151">Associare l'oggetto dispositivo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-151">Bind the device object to the device.</span></span> <span data-ttu-id="1fe1d-152">Questa operazione viene eseguita quando un'applicazione chiama [**ID3DX11ThreadPump::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), che consente di associare al dispositivo un numero specificato di oggetti nella coda degli oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-152">This is done when one's application calls [**ID3DX11ThreadPump::ProcessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), which will bind a specified number of objects in the queue of device objects to the device.</span></span>

<span data-ttu-id="1fe1d-153">La pompa di thread può essere usata per caricare i dati in uno dei due modi seguenti: chiamando un'API che accetta un thread Pump come parametro, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), oppure chiamando [**ID3DX11ThreadPump:: AddWorkItem**](id3dx11threadpump-addworkitem.md).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-153">The thread pump can be used to load data in one of two ways: by calling an API that takes a thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), or by calling [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md).</span></span> <span data-ttu-id="1fe1d-154">Nel caso delle API che accettano un thread Pump, il caricatore di dati e il processore di dati vengono creati internamente.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-154">In the case of the APIs that take a thread pump, the data loader and data processor are created internally.</span></span> <span data-ttu-id="1fe1d-155">Nel caso di AddWorkItem, il caricatore di dati e il processore di dati devono essere creati in anticipo e vengono quindi passati in AddWorkItem.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-155">In the case of AddWorkItem, the data loader and data processor must be created beforehand and are then passed into AddWorkItem.</span></span> <span data-ttu-id="1fe1d-156">D3DX11 fornisce un set di API per la creazione di caricatori di dati e processori di dati con funzionalità per il caricamento e l'elaborazione di formati di dati comuni.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-156">D3DX11 provides a set of APIs for creating data loaders and data processors that have functionality for loading and processing common data formats.</span></span> <span data-ttu-id="1fe1d-157">Per i formati di dati personalizzati, le interfacce del caricatore di dati e del processore di dati devono essere ereditate e i relativi metodi devono essere ridefiniti.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-157">For custom data formats, the data loader and data processor interfaces must be inherited and their methods must be redefined.</span></span>

<span data-ttu-id="1fe1d-158">L'oggetto della pompa di thread occupa una quantità sostanziale di risorse, quindi in genere è necessario crearne solo una per ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-158">The thread pump object takes up a substantial amount of resources, so generally only one should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe1d-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fe1d-159">Requirements</span></span>



| <span data-ttu-id="1fe1d-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fe1d-160">Requirement</span></span> | <span data-ttu-id="1fe1d-161">Valore</span><span class="sxs-lookup"><span data-stu-id="1fe1d-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe1d-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fe1d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe1d-163">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1fe1d-163">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1fe1d-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fe1d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe1d-165">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fe1d-165">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1fe1d-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fe1d-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fe1d-167"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fe1d-167"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="1fe1d-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="1fe1d-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fe1d-169"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fe1d-169"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fe1d-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fe1d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe1d-171">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="1fe1d-171">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 


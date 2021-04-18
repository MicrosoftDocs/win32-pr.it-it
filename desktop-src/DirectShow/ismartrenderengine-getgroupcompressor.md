---
description: Il metodo GetGroupCompressor Recupera il filtro di compressione per il gruppo specificato.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Metodo ISmartRenderEngine:: GetGroupCompressor (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328610"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a><span data-ttu-id="bd962-103">Metodo ISmartRenderEngine:: GetGroupCompressor</span><span class="sxs-lookup"><span data-stu-id="bd962-103">ISmartRenderEngine::GetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="bd962-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bd962-104">\[Deprecated.</span></span> <span data-ttu-id="bd962-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bd962-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bd962-106">Il `GetGroupCompressor` metodo recupera il filtro di compressione per il gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="bd962-106">The `GetGroupCompressor` method retrieves the compression filter for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd962-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd962-107">Syntax</span></span>


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="bd962-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd962-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd962-109">*Gruppo*</span><span class="sxs-lookup"><span data-stu-id="bd962-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="bd962-110">Indice in base zero del gruppo.</span><span class="sxs-lookup"><span data-stu-id="bd962-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="bd962-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="bd962-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="bd962-112">Riceve un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di compressione.</span><span class="sxs-lookup"><span data-stu-id="bd962-112">Receives a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span> <span data-ttu-id="bd962-113">Riceve il valore **null** se non è presente alcun filtro di compressione.</span><span class="sxs-lookup"><span data-stu-id="bd962-113">It receives the value **NULL** if there is no compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd962-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd962-114">Return value</span></span>

<span data-ttu-id="bd962-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bd962-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd962-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd962-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd962-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd962-117">Remarks</span></span>

<span data-ttu-id="bd962-118">Utilizzare questo metodo per impostare le proprietà sul filtro di compressione, ad esempio la frequenza dei fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="bd962-118">Use this method to set properties on the compression filter, such as the key-frame rate.</span></span> <span data-ttu-id="bd962-119">Chiamare questo metodo dopo la chiamata a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md), ma prima di eseguire il rendering del progetto.</span><span class="sxs-lookup"><span data-stu-id="bd962-119">Call this method after calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), but before rendering the project.</span></span> <span data-ttu-id="bd962-120">Eseguire quindi una query sul pin di output del filtro di compressione per l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , che contiene i metodi per l'impostazione dei parametri di compressione.</span><span class="sxs-lookup"><span data-stu-id="bd962-120">Then query the compression filter's output pin for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, which contains methods for setting compression parameters.</span></span> <span data-ttu-id="bd962-121">Al termine, rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="bd962-121">Release the interface when you are done.</span></span> <span data-ttu-id="bd962-122">Se si apportano modifiche successive alla sequenza temporale, chiamare **ConnectFrontEnd**, quindi chiamare di nuovo **GetGroupCompressor** per reimpostare i parametri di compressione.</span><span class="sxs-lookup"><span data-stu-id="bd962-122">If you make any subsequent changes to the timeline, call **ConnectFrontEnd**, and then call **GetGroupCompressor** again to reset the compression parameters.</span></span>

<span data-ttu-id="bd962-123">In caso di restituzione, se il valore di \* *pCompressor* è diverso da **null**, l'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="bd962-123">On return, if the value of \**pCompressor* is non-**NULL**, the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface has an outstanding reference count.</span></span> <span data-ttu-id="bd962-124">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="bd962-124">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="bd962-125">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="bd962-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bd962-126">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd962-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bd962-127">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bd962-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd962-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd962-128">Requirements</span></span>



| <span data-ttu-id="bd962-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd962-129">Requirement</span></span> | <span data-ttu-id="bd962-130">Valore</span><span class="sxs-lookup"><span data-stu-id="bd962-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd962-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd962-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bd962-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd962-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bd962-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="bd962-133">Library</span></span><br/> | <dl> <span data-ttu-id="bd962-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd962-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd962-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd962-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd962-136">**Interfaccia ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="bd962-136">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="bd962-137">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="bd962-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





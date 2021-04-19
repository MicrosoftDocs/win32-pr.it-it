---
description: Il metodo SetResizerGUID specifica il CLSID di un filtro di ridimensionamento video personalizzato.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'Metodo IRenderEngine2:: SetResizerGUID (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332575"
---
# <a name="irenderengine2setresizerguid-method"></a><span data-ttu-id="c4db0-103">Metodo IRenderEngine2:: SetResizerGUID</span><span class="sxs-lookup"><span data-stu-id="c4db0-103">IRenderEngine2::SetResizerGUID method</span></span>

> [!Note]  
> <span data-ttu-id="c4db0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c4db0-104">\[Deprecated.</span></span> <span data-ttu-id="c4db0-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4db0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4db0-106">Il `SetResizerGUID` metodo specifica il CLSID di un filtro di ridimensionamento video personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c4db0-106">The `SetResizerGUID` method specifies the CLSID of a custom video resizing filter.</span></span> <span data-ttu-id="c4db0-107">Chiamare questo metodo per sostituire il filtro di ridimensionamento predefinito utilizzato dai servizi di modifica DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c4db0-107">Call this method to replace the default resizing filter used by DirectShow Editing Services.</span></span> <span data-ttu-id="c4db0-108">Il filtro deve essere registrato come oggetto COM nel sistema dell'utente e deve supportare l'interfaccia [**IResize**](iresize.md) .</span><span class="sxs-lookup"><span data-stu-id="c4db0-108">Your filter must be registered as a COM object on the user's system, and it must support the [**IResize**](iresize.md) interface.</span></span>

<span data-ttu-id="c4db0-109">Chiamare questo metodo prima di chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="c4db0-109">Call this method before calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4db0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4db0-110">Syntax</span></span>


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a><span data-ttu-id="c4db0-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4db0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4db0-112">*ResizerGuid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4db0-112">*ResizerGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4db0-113">CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="c4db0-113">The CLSID of the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4db0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4db0-114">Return value</span></span>

<span data-ttu-id="c4db0-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4db0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4db0-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4db0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4db0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4db0-117">Remarks</span></span>

<span data-ttu-id="c4db0-118">Per ripristinare il valore predefinito DES Resizer, usare il CLSID seguente:</span><span class="sxs-lookup"><span data-stu-id="c4db0-118">To revert to the default DES resizer, use the following CLSID:</span></span>


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> <span data-ttu-id="c4db0-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c4db0-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c4db0-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4db0-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c4db0-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c4db0-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4db0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4db0-122">Requirements</span></span>



| <span data-ttu-id="c4db0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4db0-123">Requirement</span></span> | <span data-ttu-id="c4db0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c4db0-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4db0-125">Versione</span><span class="sxs-lookup"><span data-stu-id="c4db0-125">Version</span></span><br/> | <span data-ttu-id="c4db0-126">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c4db0-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="c4db0-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4db0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c4db0-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4db0-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c4db0-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4db0-129">Library</span></span><br/> | <dl> <span data-ttu-id="c4db0-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4db0-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4db0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4db0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4db0-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c4db0-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="c4db0-133">**Interfaccia IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="c4db0-133">**IRenderEngine2 Interface**</span></span>](irenderengine2.md)
</dt> </dl>

 

 





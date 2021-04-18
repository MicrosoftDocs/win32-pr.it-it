---
title: Metodo getinclusion IWMDRMLicense (wmdrmsdk. h)
description: Il metodo getinclusivion recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Formato di Windows Media (metodo getinclusiont)
- Metodo getincludent Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo getinclusivion
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324282"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a><span data-ttu-id="7058b-106">Metodo IWMDRMLicense:: getinclusivion</span><span class="sxs-lookup"><span data-stu-id="7058b-106">IWMDRMLicense::GetInclusionList method</span></span>

<span data-ttu-id="7058b-107">Il metodo **Getinclusivion** recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.</span><span class="sxs-lookup"><span data-stu-id="7058b-107">The **GetInclusionList** method retrieves the entire inclusion list for the current license or license chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="7058b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7058b-108">Syntax</span></span>


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a><span data-ttu-id="7058b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7058b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7058b-110">*ppGuids* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7058b-110">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7058b-111">Riceve una matrice di GUID che identifica le tecnologie incluse.</span><span class="sxs-lookup"><span data-stu-id="7058b-111">Receives an array of GUIDs identifying the included technologies.</span></span>

</dd> <dt>

<span data-ttu-id="7058b-112">*pcGuids* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7058b-112">*pcGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7058b-113">Riceve il numero di elementi nella matrice *ppGuids* .</span><span class="sxs-lookup"><span data-stu-id="7058b-113">Receives the number of elements in the *ppGuids* array.</span></span> <span data-ttu-id="7058b-114">La matrice viene allocata usando **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="7058b-114">The array is allocated by using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="7058b-115">Al termine dell'elenco, rilasciare la memoria chiamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="7058b-115">When finished with the list, release the memory by calling **CoTaskMemFree**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7058b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7058b-116">Return value</span></span>

<span data-ttu-id="7058b-117">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7058b-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7058b-118">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7058b-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7058b-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7058b-119">Return code</span></span>                                                                          | <span data-ttu-id="7058b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7058b-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7058b-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7058b-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7058b-122">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7058b-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7058b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7058b-123">Remarks</span></span>

<span data-ttu-id="7058b-124">L'emittente della licenza può specificare altri sistemi di protezione in cui è possibile convertire il contenuto crittografato.</span><span class="sxs-lookup"><span data-stu-id="7058b-124">The license issuer can specify other protection systems to which the encrypted content may be converted.</span></span> <span data-ttu-id="7058b-125">L'elenco di GUID recuperato da questo metodo identifica i sistemi di protezione consentiti.</span><span class="sxs-lookup"><span data-stu-id="7058b-125">The list of GUIDs retrieved by this method identifies the allowed protection systems.</span></span> <span data-ttu-id="7058b-126">Quando si immette in un contratto di licenza con Microsoft per ottenere la libreria stub, si riceverà un elenco dei sistemi di protezione attualmente supportati e i GUID usati per identificarli.</span><span class="sxs-lookup"><span data-stu-id="7058b-126">When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.</span></span>

## <a name="requirements"></a><span data-ttu-id="7058b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7058b-127">Requirements</span></span>



| <span data-ttu-id="7058b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7058b-128">Requirement</span></span> | <span data-ttu-id="7058b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7058b-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7058b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7058b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7058b-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7058b-131"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="7058b-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="7058b-132">Library</span></span><br/> | <dl> <span data-ttu-id="7058b-133"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7058b-133"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7058b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7058b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7058b-135">**Elenchi di inclusione e autorizzazione esplicita**</span><span class="sxs-lookup"><span data-stu-id="7058b-135">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="7058b-136">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="7058b-136">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 






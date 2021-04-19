---
description: Il \_ metodo Get Item restituisce l'attributo specificato dall'indice.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'Metodo ITAttributeList:: get_Item (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332730"
---
# <a name="itattributelistget_item-method"></a><span data-ttu-id="7facb-103">Metodo ITAttributeList:: Get \_ Item</span><span class="sxs-lookup"><span data-stu-id="7facb-103">ITAttributeList::get\_Item method</span></span>

<span data-ttu-id="7facb-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7facb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7facb-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7facb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7facb-106">Il metodo **get \_ Item** restituisce l'attributo specificato dall'indice.</span><span class="sxs-lookup"><span data-stu-id="7facb-106">The **get\_Item** method returns the attribute specified by the index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7facb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7facb-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7facb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7facb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7facb-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7facb-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7facb-110">Indice dell'elemento da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7facb-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="7facb-111">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7facb-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7facb-112">Puntatore a un **BSTR** che contiene i valori dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7facb-112">Pointer to a **BSTR** containing the values of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7facb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7facb-113">Return value</span></span>

<span data-ttu-id="7facb-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7facb-114">This method can return one of these values.</span></span>



| <span data-ttu-id="7facb-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7facb-115">Return code</span></span>                                                                                   | <span data-ttu-id="7facb-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7facb-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7facb-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7facb-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7facb-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7facb-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7facb-120">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="7facb-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="7facb-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7facb-122">Il parametro di *Indice* non è valido.</span><span class="sxs-lookup"><span data-stu-id="7facb-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="7facb-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7facb-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7facb-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7facb-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7facb-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7facb-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7facb-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7facb-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="7facb-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7facb-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="7facb-129">Remarks</span></span>

<span data-ttu-id="7facb-130">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *pval* .</span><span class="sxs-lookup"><span data-stu-id="7facb-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *pVal* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7facb-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7facb-131">Requirements</span></span>



| <span data-ttu-id="7facb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7facb-132">Requirement</span></span> | <span data-ttu-id="7facb-133">Valore</span><span class="sxs-lookup"><span data-stu-id="7facb-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7facb-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7facb-134">TAPI version</span></span><br/> | <span data-ttu-id="7facb-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7facb-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7facb-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7facb-136">Header</span></span><br/>       | <dl> <span data-ttu-id="7facb-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7facb-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="7facb-138">Library</span></span><br/>      | <dl> <span data-ttu-id="7facb-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7facb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7facb-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="7facb-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7facb-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7facb-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7facb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7facb-143">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="7facb-143">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 


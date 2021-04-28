---
description: 'Metodo ITTimeCollection::get__NewEnum : il metodo get \_ \_ NewEnum restituisce un enumeratore per la raccolta.'
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: Metodo ITTimeCollection::get__NewEnum (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acfc9d616efb58c6173f2c9c6e5913d27776958c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088889"
---
# <a name="ittimecollectionget__newenum-method"></a><span data-ttu-id="70ae2-103">Metodo ITTimeCollection::get \_ \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="70ae2-103">ITTimeCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="70ae2-104">\[ Le interfacce e i controlli di conferenza di telefonia IP di Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="70ae2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="70ae2-105">L'API client rtc offre funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="70ae2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="70ae2-106">Il **metodo get \_ \_ NewEnum** restituisce un enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="70ae2-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ae2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70ae2-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="70ae2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="70ae2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70ae2-109">*pVal* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="70ae2-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70ae2-110">Puntatore a [un'interfaccia IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) su un oggetto enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="70ae2-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="70ae2-111">Chiamare il [metodo QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia **IUnknown** restituita per ottenere un puntatore a [un'interfaccia di enumerazione IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="70ae2-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="70ae2-112">**IEnumVARIANT fornisce** una serie di metodi che è possibile usare per scorrere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="70ae2-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="70ae2-113">Per ulteriori informazioni, vedere la sezione Osservazioni successiva.</span><span class="sxs-lookup"><span data-stu-id="70ae2-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70ae2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70ae2-114">Return value</span></span>

<span data-ttu-id="70ae2-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="70ae2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="70ae2-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="70ae2-116">Return code</span></span>                                                                                   | <span data-ttu-id="70ae2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70ae2-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="70ae2-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="70ae2-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="70ae2-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="70ae2-120"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="70ae2-121">Il *parametro pVal* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="70ae2-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="70ae2-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="70ae2-123">Memoria insufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="70ae2-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="70ae2-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="70ae2-125">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="70ae2-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="70ae2-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="70ae2-127">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="70ae2-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="70ae2-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="70ae2-128">Remarks</span></span>

<span data-ttu-id="70ae2-129">Questo metodo è intercambiabile con [**get \_ EnumerationIf,**](ittimecollection-get-enumerationif.md) ad eccezione del fatto che restituisce **IUnknown** anziché [**IEnumTime.**](ienumtime.md)</span><span class="sxs-lookup"><span data-stu-id="70ae2-129">This method is interchangeable with [**get\_EnumerationIf**](ittimecollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumTime**](ienumtime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70ae2-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70ae2-130">Requirements</span></span>



| <span data-ttu-id="70ae2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ae2-131">Requirement</span></span> | <span data-ttu-id="70ae2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="70ae2-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70ae2-133">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="70ae2-133">TAPI version</span></span><br/> | <span data-ttu-id="70ae2-134">Richiede TAPI 3.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="70ae2-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="70ae2-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70ae2-135">Header</span></span><br/>       | <dl> <span data-ttu-id="70ae2-136"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="70ae2-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="70ae2-137">Library</span></span><br/>      | <dl> <span data-ttu-id="70ae2-138"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="70ae2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="70ae2-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="70ae2-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70ae2-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ae2-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70ae2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ae2-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="70ae2-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="70ae2-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="70ae2-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 


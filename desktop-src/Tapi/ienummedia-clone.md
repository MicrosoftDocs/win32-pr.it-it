---
description: 'Metodo IEnumMedia::Clone: il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: Metodo IEnumMedia::Clone (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114549"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="f2c48-103">Metodo IEnumMedia::Clone</span><span class="sxs-lookup"><span data-stu-id="f2c48-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="f2c48-104">\[ Le interfacce e i controlli di conferenza di telefonia IP di Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f2c48-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f2c48-105">L'API client rtc offre funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f2c48-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f2c48-106">Il **metodo Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="f2c48-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c48-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2c48-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="f2c48-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2c48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c48-109">*ppEnum* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="f2c48-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c48-110">Puntatore al nuovo [**oggetto IEnumMedia.**](ienummedia.md)</span><span class="sxs-lookup"><span data-stu-id="f2c48-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c48-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2c48-111">Return value</span></span>

<span data-ttu-id="f2c48-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f2c48-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f2c48-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f2c48-113">Value</span></span>                                                                                         | <span data-ttu-id="f2c48-114">Significato</span><span class="sxs-lookup"><span data-stu-id="f2c48-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f2c48-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c48-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f2c48-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f2c48-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f2c48-117"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c48-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f2c48-118">Il *parametro ppEnum* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="f2c48-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="f2c48-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c48-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f2c48-120">Memoria insufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f2c48-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f2c48-121"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c48-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="f2c48-122">Operazione non riuscita per motivi sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="f2c48-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="f2c48-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2c48-123">Remarks</span></span>

<span data-ttu-id="f2c48-124">TAPI chiama il **metodo AddRef** sull'interfaccia [**IEnumMedia**](ienummedia.md) restituita da **IEnumMedia::Clone.**</span><span class="sxs-lookup"><span data-stu-id="f2c48-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="f2c48-125">L'applicazione deve **chiamare Release** **sull'interfaccia IEnumMedia** per liberare le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="f2c48-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c48-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2c48-126">Requirements</span></span>



| <span data-ttu-id="f2c48-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c48-127">Requirement</span></span> | <span data-ttu-id="f2c48-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f2c48-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c48-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f2c48-129">TAPI version</span></span><br/> | <span data-ttu-id="f2c48-130">Richiede TAPI 3.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f2c48-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f2c48-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2c48-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f2c48-132"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c48-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2c48-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2c48-133">Library</span></span><br/>      | <dl> <span data-ttu-id="f2c48-134"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2c48-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f2c48-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f2c48-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="f2c48-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2c48-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2c48-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2c48-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c48-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="f2c48-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 





---
description: Il metodo GetCurrentFormat Recupera il formato multimediale del flusso corrente.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'Metodo ITFormatControl:: GetCurrentFormat (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329460"
---
# <a name="itformatcontrolgetcurrentformat-method"></a><span data-ttu-id="5ec5b-103">Metodo ITFormatControl:: GetCurrentFormat</span><span class="sxs-lookup"><span data-stu-id="5ec5b-103">ITFormatControl::GetCurrentFormat method</span></span>

<span data-ttu-id="5ec5b-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5ec5b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="5ec5b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5ec5b-106">Il metodo **GetCurrentFormat** Recupera il formato multimediale del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-106">The **GetCurrentFormat** method retrieves the media format of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec5b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ec5b-107">Syntax</span></span>


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="5ec5b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ec5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec5b-109">*ppMediaType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ec5b-109">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec5b-110">Puntatore a un descrittore del **\_ \_ tipo di supporto am** del formato terminale.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="5ec5b-111">Per ulteriori informazioni sul **\_ \_ tipo di supporto am**, vedere la documentazione di DirectX.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec5b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ec5b-112">Return value</span></span>

<span data-ttu-id="5ec5b-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-113">This method can return one of these values.</span></span>



| <span data-ttu-id="5ec5b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5ec5b-114">Return code</span></span>                                                                                   | <span data-ttu-id="5ec5b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec5b-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5ec5b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec5b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5ec5b-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5ec5b-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec5b-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5ec5b-119">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5ec5b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ec5b-120">Requirements</span></span>



| <span data-ttu-id="5ec5b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec5b-121">Requirement</span></span> | <span data-ttu-id="5ec5b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5ec5b-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec5b-123">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5ec5b-123">TAPI version</span></span><br/> | <span data-ttu-id="5ec5b-124">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="5ec5b-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="5ec5b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ec5b-125">Header</span></span><br/>       | <dl> <span data-ttu-id="5ec5b-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec5b-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ec5b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ec5b-127">Library</span></span><br/>      | <dl> <span data-ttu-id="5ec5b-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ec5b-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="5ec5b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5ec5b-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="5ec5b-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ec5b-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec5b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ec5b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec5b-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="5ec5b-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 





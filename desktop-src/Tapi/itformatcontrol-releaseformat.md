---
description: Il metodo ReleaseFormat rilascia la struttura associata al formato.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'Metodo ITFormatControl:: ReleaseFormat (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329452"
---
# <a name="itformatcontrolreleaseformat-method"></a><span data-ttu-id="0b92b-103">Metodo ITFormatControl:: ReleaseFormat</span><span class="sxs-lookup"><span data-stu-id="0b92b-103">ITFormatControl::ReleaseFormat method</span></span>

<span data-ttu-id="0b92b-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b92b-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0b92b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0b92b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0b92b-106">Il metodo **ReleaseFormat** rilascia la struttura associata al formato.</span><span class="sxs-lookup"><span data-stu-id="0b92b-106">The **ReleaseFormat** method releases the structure associated with the format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b92b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b92b-107">Syntax</span></span>


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="0b92b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b92b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b92b-109">*pMediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b92b-109">*pMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b92b-110">Puntatore a un descrittore del **\_ \_ tipo di supporto am** del formato terminale.</span><span class="sxs-lookup"><span data-stu-id="0b92b-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="0b92b-111">Per ulteriori informazioni sul **\_ \_ tipo di supporto am**, vedere la documentazione di DirectX.</span><span class="sxs-lookup"><span data-stu-id="0b92b-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b92b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b92b-112">Return value</span></span>

<span data-ttu-id="0b92b-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0b92b-113">This method can return one of these values.</span></span>



| <span data-ttu-id="0b92b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0b92b-114">Return code</span></span>                                                                                   | <span data-ttu-id="0b92b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b92b-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0b92b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b92b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b92b-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0b92b-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0b92b-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0b92b-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b92b-119">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0b92b-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0b92b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b92b-120">Requirements</span></span>



| <span data-ttu-id="0b92b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b92b-121">Requirement</span></span> | <span data-ttu-id="0b92b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0b92b-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0b92b-123">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0b92b-123">TAPI version</span></span><br/> | <span data-ttu-id="0b92b-124">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="0b92b-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="0b92b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b92b-125">Header</span></span><br/>       | <dl> <span data-ttu-id="0b92b-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b92b-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b92b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b92b-127">Library</span></span><br/>      | <dl> <span data-ttu-id="0b92b-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b92b-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="0b92b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0b92b-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="0b92b-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b92b-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b92b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b92b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b92b-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="0b92b-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 





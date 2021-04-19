---
title: Metodo Encrypt IWMSecureBuffer (wmdrmsdk. h)
description: Il metodo Encrypt crittografa un puntatore di dati.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Metodo Encrypt formato Windows Media
- Metodo Encrypt formato Windows Media, interfaccia IWMSecureBuffer
- Interfaccia IWMSecureBuffer-formato Windows Media, metodo Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333621"
---
# <a name="iwmsecurebufferencrypt-method"></a><span data-ttu-id="d5342-106">Metodo IWMSecureBuffer:: Encrypt</span><span class="sxs-lookup"><span data-stu-id="d5342-106">IWMSecureBuffer::Encrypt method</span></span>

<span data-ttu-id="d5342-107">Il metodo **Encrypt** crittografa un puntatore di dati.</span><span class="sxs-lookup"><span data-stu-id="d5342-107">The **Encrypt** method encrypts a data pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5342-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5342-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="d5342-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5342-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5342-110">*pSecureChannel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5342-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5342-111">Puntatore a un'interfaccia di canale sicura che contiene il puntatore ai dati da crittografare.</span><span class="sxs-lookup"><span data-stu-id="d5342-111">Pointer to a secure channel interface containing the data pointer to encrypt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5342-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5342-112">Return value</span></span>

<span data-ttu-id="d5342-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d5342-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d5342-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d5342-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d5342-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d5342-115">Return code</span></span>                                                                          | <span data-ttu-id="d5342-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5342-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d5342-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5342-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d5342-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d5342-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5342-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5342-119">Remarks</span></span>

<span data-ttu-id="d5342-120">Utilizzare questo metodo per crittografare i puntatori dati in modo che possano essere inviati attraverso i limiti DLL.</span><span class="sxs-lookup"><span data-stu-id="d5342-120">Use this method to encrypt data pointers so they can be sent across DLL boundaries.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5342-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5342-121">Requirements</span></span>



| <span data-ttu-id="d5342-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5342-122">Requirement</span></span> | <span data-ttu-id="d5342-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d5342-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5342-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5342-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5342-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5342-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5342-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5342-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5342-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5342-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5342-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5342-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5342-129">**Decrypt**</span><span class="sxs-lookup"><span data-stu-id="d5342-129">**Decrypt**</span></span>](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[<span data-ttu-id="d5342-130">**Interfaccia IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5342-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 






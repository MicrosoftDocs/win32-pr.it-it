---
title: Metodo Decrypt IWMSecureBuffer (wmdrmsdk. h)
description: Il metodo Decrypt decrittografa un puntatore a dati crittografato chiamando il metodo Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Metodo Decrypt Windows Media Format
- Metodo di decrittografia Windows Media Format, interfaccia IWMSecureBuffer
- Interfaccia IWMSecureBuffer-formato Windows Media, metodo Decrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333623"
---
# <a name="iwmsecurebufferdecrypt-method"></a><span data-ttu-id="2baef-106">IWMSecureBuffer::D Metodo ecrypt</span><span class="sxs-lookup"><span data-stu-id="2baef-106">IWMSecureBuffer::Decrypt method</span></span>

<span data-ttu-id="2baef-107">Il metodo **Decrypt** decrittografa un puntatore a dati crittografato chiamando il metodo [**Encrypt**](iwmsecurebuffer-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="2baef-107">The **Decrypt** method decrypts a data pointer that was encrypted by calling the [**Encrypt**](iwmsecurebuffer-encrypt.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2baef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2baef-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="2baef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2baef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2baef-110">*pSecureChannel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2baef-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2baef-111">Puntatore a un'interfaccia di canale sicura che contiene il puntatore ai dati crittografati.</span><span class="sxs-lookup"><span data-stu-id="2baef-111">Pointer to a secure channel interface containing the encrypted data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2baef-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2baef-112">Return value</span></span>

<span data-ttu-id="2baef-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2baef-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2baef-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2baef-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2baef-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2baef-115">Return code</span></span>                                                                          | <span data-ttu-id="2baef-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2baef-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2baef-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2baef-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2baef-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2baef-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2baef-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2baef-119">Remarks</span></span>

<span data-ttu-id="2baef-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="2baef-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="2baef-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2baef-121">Requirements</span></span>



| <span data-ttu-id="2baef-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2baef-122">Requirement</span></span> | <span data-ttu-id="2baef-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2baef-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2baef-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2baef-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2baef-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2baef-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="2baef-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="2baef-126">Library</span></span><br/> | <dl> <span data-ttu-id="2baef-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2baef-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2baef-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2baef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2baef-129">**Crittografare**</span><span class="sxs-lookup"><span data-stu-id="2baef-129">**Encrypt**</span></span>](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[<span data-ttu-id="2baef-130">**Interfaccia IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="2baef-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 






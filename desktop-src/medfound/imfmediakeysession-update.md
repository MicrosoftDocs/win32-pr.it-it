---
description: Passa un valore di chiave con tutti i dati associati richiesti dal modulo di decrittografia del contenuto per il sistema di chiavi specificato.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'Metodo IMFMediaKeySession:: Update'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320788"
---
# <a name="imfmediakeysessionupdate-method"></a><span data-ttu-id="dcd08-103">Metodo IMFMediaKeySession:: Update</span><span class="sxs-lookup"><span data-stu-id="dcd08-103">IMFMediaKeySession::Update method</span></span>

<span data-ttu-id="dcd08-104">Passa un valore di chiave con tutti i dati associati richiesti dal modulo di decrittografia del contenuto per il sistema di chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="dcd08-104">Passes in a key value with any associated data required by the Content Decryption Module for the given key system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd08-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcd08-105">Syntax</span></span>


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a><span data-ttu-id="dcd08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcd08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd08-107">*key*</span><span class="sxs-lookup"><span data-stu-id="dcd08-107">*key*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="dcd08-108">*CB*</span><span class="sxs-lookup"><span data-stu-id="dcd08-108">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd08-109">Conteggio in byte della *chiave*.</span><span class="sxs-lookup"><span data-stu-id="dcd08-109">The count in bytes of *key*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcd08-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcd08-110">Return value</span></span>

<span data-ttu-id="dcd08-111">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dcd08-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dcd08-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd08-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcd08-113">Requirements</span></span>



| <span data-ttu-id="dcd08-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcd08-114">Requirement</span></span> | <span data-ttu-id="dcd08-115">Valore</span><span class="sxs-lookup"><span data-stu-id="dcd08-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd08-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcd08-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd08-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcd08-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dcd08-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcd08-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd08-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcd08-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dcd08-120">IDL</span><span class="sxs-lookup"><span data-stu-id="dcd08-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dcd08-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dcd08-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcd08-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcd08-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd08-123">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="dcd08-123">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 





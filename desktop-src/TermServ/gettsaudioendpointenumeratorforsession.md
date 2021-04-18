---
title: Funzione di callback GetTSAudioEndpointEnumeratorForSession
description: Restituisce un riferimento a un enumeratore di endpoint audio per l'ID sessione specificato.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Funzione di callback GetTSAudioEndpointEnumeratorForSession Servizi Desktop remoto
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302471"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a><span data-ttu-id="2151c-104">Funzione di callback GetTSAudioEndpointEnumeratorForSession</span><span class="sxs-lookup"><span data-stu-id="2151c-104">GetTSAudioEndpointEnumeratorForSession callback function</span></span>

<span data-ttu-id="2151c-105">Restituisce un riferimento a un enumeratore di endpoint audio per l'ID sessione specificato.</span><span class="sxs-lookup"><span data-stu-id="2151c-105">Returns a reference to an audio endpoint enumerator for the specified session ID.</span></span> <span data-ttu-id="2151c-106">I consumer di questo enumeratore di endpoint audio, ad esempio MMDevAPI.dll, chiamano questa funzione per recuperare un enumeratore di endpoint audio in una sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2151c-106">Consumers of this audio endpoint enumerator, such as MMDevAPI.dll, call this function to retrieve an audio endpoint enumerator in a Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="2151c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2151c-107">Syntax</span></span>


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="2151c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2151c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2151c-109">*ID sessione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2151c-109">*SessionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2151c-110">Identificatore della sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2151c-110">The identifier of the Remote Desktop Services session.</span></span>

</dd> <dt>

<span data-ttu-id="2151c-111">*ppEndpointEnumerator* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2151c-111">*ppEndpointEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2151c-112">Indirizzo di un puntatore a un'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="2151c-112">The address of a pointer to an [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2151c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2151c-113">Return value</span></span>

<span data-ttu-id="2151c-114">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2151c-114">If the method succeeds, it returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2151c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2151c-115">Remarks</span></span>

<span data-ttu-id="2151c-116">Questa funzione non è definita in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="2151c-116">This function is not defined in a header file.</span></span> <span data-ttu-id="2151c-117">È necessario implementare ed esportare questa funzione nell'enumeratore dell'endpoint personalizzato e utilizzare la firma mostrata nel blocco della sintassi più indietro in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="2151c-117">You should implement and export this function in your custom endpoint enumerator and use the signature shown in the syntax block earlier in this topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="2151c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2151c-118">Requirements</span></span>



| <span data-ttu-id="2151c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2151c-119">Requirement</span></span> | <span data-ttu-id="2151c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2151c-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="2151c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2151c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2151c-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2151c-122">None supported</span></span><br/>         |
| <span data-ttu-id="2151c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2151c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2151c-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2151c-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2151c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2151c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2151c-126">Implementazione di un enumeratore di endpoint audio personalizzato</span><span class="sxs-lookup"><span data-stu-id="2151c-126">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[<span data-ttu-id="2151c-127">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="2151c-127">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 


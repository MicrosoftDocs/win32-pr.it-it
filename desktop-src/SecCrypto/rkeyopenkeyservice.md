---
description: La funzione RKeyOpenKeyService non è supportata.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Funzione RKeyOpenKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314692"
---
# <a name="rkeyopenkeyservice-function"></a><span data-ttu-id="32087-103">RKeyOpenKeyService (funzione)</span><span class="sxs-lookup"><span data-stu-id="32087-103">RKeyOpenKeyService function</span></span>

<span data-ttu-id="32087-104">La funzione **RKeyOpenKeyService** non è supportata.</span><span class="sxs-lookup"><span data-stu-id="32087-104">The **RKeyOpenKeyService** function is not supported.</span></span>

<span data-ttu-id="32087-105">**Windows Server 2003:** La funzione **RKeyOpenKeyService** stabilisce una connessione a un computer remoto e apre un handle del servizio Key.</span><span class="sxs-lookup"><span data-stu-id="32087-105">**Windows Server 2003:** The **RKeyOpenKeyService** function establishes a connection to a remote computer and opens a key service handle.</span></span> <span data-ttu-id="32087-106">L'handle del servizio chiave può essere successivamente usato dalla funzione [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="32087-106">The key service handle can subsequently be used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span> <span data-ttu-id="32087-107">Si noti che questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="32087-107">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="32087-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32087-108">Syntax</span></span>


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a><span data-ttu-id="32087-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="32087-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32087-110">*pszMachineName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32087-110">*pszMachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32087-111">Puntatore long a una stringa con terminazione null che rappresenta il computer in cui verrà aperto l'handle del servizio di chiave.</span><span class="sxs-lookup"><span data-stu-id="32087-111">Long pointer to a null-terminated string that represents the computer where the key service handle will be opened.</span></span>

</dd> <dt>

<span data-ttu-id="32087-112">*TipoProprietario* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32087-112">*OwnerType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32087-113">[**KEYSVC \_**](keysvc-type.md) Valore di tipo che rappresenta il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="32087-113">[**KEYSVC\_TYPE**](keysvc-type.md) value that represents the key type.</span></span> <span data-ttu-id="32087-114">L'unico valore supportato è **KeySvcMachine**.</span><span class="sxs-lookup"><span data-stu-id="32087-114">The only supported value is **KeySvcMachine**.</span></span>

</dd> <dt>

<span data-ttu-id="32087-115">*pwszOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32087-115">*pwszOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32087-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="32087-116">Reserved.</span></span> <span data-ttu-id="32087-117">Impostare questo valore su **null**.</span><span class="sxs-lookup"><span data-stu-id="32087-117">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="32087-118">*pAuthentication* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32087-118">*pAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32087-119">Puntatore a un **void** che rappresenta le impostazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="32087-119">A pointer to a **void** that represents the authentication settings.</span></span> <span data-ttu-id="32087-120">Questo puntatore può puntare a un valore pari a zero o al valore seguente.</span><span class="sxs-lookup"><span data-stu-id="32087-120">This pointer can point to a value of zero or the following value.</span></span>



| <span data-ttu-id="32087-121">Valore</span><span class="sxs-lookup"><span data-stu-id="32087-121">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="32087-122">Significato</span><span class="sxs-lookup"><span data-stu-id="32087-122">Meaning</span></span>                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <span data-ttu-id="32087-123"><dt>**RKEYSVC \_ Connetti \_ \_ solo sicuro**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="32087-123"><dt>**RKEYSVC\_CONNECT\_SECURE\_ONLY**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="32087-124">Il client richiede l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="32087-124">The client requires mutual authentication.</span></span> <span data-ttu-id="32087-125">Se viene specificato questo valore, il fallback a NTLM avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="32087-125">If this value is specified, fallback to NTLM will fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="32087-126">*mantenuta* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="32087-126">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32087-127">Riservato.</span><span class="sxs-lookup"><span data-stu-id="32087-127">Reserved.</span></span> <span data-ttu-id="32087-128">Impostare questo valore su **null**.</span><span class="sxs-lookup"><span data-stu-id="32087-128">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="32087-129">*phKeySvcCli* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32087-129">*phKeySvcCli* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32087-130">Puntatore a un [**\_ handle KEYSVCC**](keysvcc-handle.md) che riceve l'handle di servizio della chiave aperta.</span><span class="sxs-lookup"><span data-stu-id="32087-130">A pointer to a [**KEYSVCC\_HANDLE**](keysvcc-handle.md) that receives the opened key service handle.</span></span> <span data-ttu-id="32087-131">Al termine dell'utilizzo dell'handle, liberare la risorsa chiamando la funzione [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="32087-131">When you have finished using the handle, free the resource by calling the [**RKeyCloseKeyService**](rkeyclosekeyservice.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32087-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32087-132">Return value</span></span>

<span data-ttu-id="32087-133">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32087-133">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="32087-134">Se la funzione ha esito negativo, il valore restituito è un **ULONG** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="32087-134">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="32087-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32087-135">Requirements</span></span>



| <span data-ttu-id="32087-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="32087-136">Requirement</span></span> | <span data-ttu-id="32087-137">Valore</span><span class="sxs-lookup"><span data-stu-id="32087-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32087-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32087-138">Minimum supported client</span></span><br/> | <span data-ttu-id="32087-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="32087-139">None supported</span></span><br/>                                                             |
| <span data-ttu-id="32087-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32087-140">Minimum supported server</span></span><br/> | <span data-ttu-id="32087-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32087-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32087-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32087-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="32087-143"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="32087-143"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32087-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32087-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32087-145">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="32087-145">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="32087-146">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="32087-146">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 





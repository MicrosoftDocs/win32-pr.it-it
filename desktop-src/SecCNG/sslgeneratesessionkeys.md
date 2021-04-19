---
description: Genera un set di chiavi di sessione SSL (Secure Sockets Layer Protocol).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Funzione SslGenerateSessionKeys (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319913"
---
# <a name="sslgeneratesessionkeys-function"></a><span data-ttu-id="ed140-103">SslGenerateSessionKeys (funzione)</span><span class="sxs-lookup"><span data-stu-id="ed140-103">SslGenerateSessionKeys function</span></span>

<span data-ttu-id="ed140-104">La funzione **SslGenerateSessionKeys** genera un set di chiavi di sessione SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="ed140-104">The **SslGenerateSessionKeys** function generates a set of [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) session keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed140-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed140-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ed140-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed140-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed140-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed140-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed140-108">Handle per l'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="ed140-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ed140-109">*hMasterKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed140-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed140-110">Handle per l'oggetto [*chiave master*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="ed140-110">The handle to the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="ed140-111">*phReadKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed140-111">*phReadKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed140-112">Puntatore all'handle della chiave di lettura restituito.</span><span class="sxs-lookup"><span data-stu-id="ed140-112">A pointer to the returned read key handle.</span></span>

</dd> <dt>

<span data-ttu-id="ed140-113">*phWriteKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed140-113">*phWriteKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed140-114">Puntatore all'handle della chiave di scrittura restituito.</span><span class="sxs-lookup"><span data-stu-id="ed140-114">A pointer to the returned write key handle.</span></span>

</dd> <dt>

<span data-ttu-id="ed140-115">*pParameterList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed140-115">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed140-116">Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni utilizzate come parte dell'operazione di scambio delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="ed140-116">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="ed140-117">Il set preciso di buffer dipende dal protocollo e dal pacchetto di crittografia utilizzati.</span><span class="sxs-lookup"><span data-stu-id="ed140-117">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="ed140-118">Come minimo, l'elenco conterrà i buffer contenenti i valori casuali specificati dal client e dal server.</span><span class="sxs-lookup"><span data-stu-id="ed140-118">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="ed140-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed140-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed140-120">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="ed140-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed140-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed140-121">Return value</span></span>

<span data-ttu-id="ed140-122">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ed140-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ed140-123">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ed140-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="ed140-124">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="ed140-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ed140-125">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed140-125">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="ed140-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed140-126">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed140-127"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="ed140-127"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="ed140-128">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="ed140-128">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="ed140-129"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ed140-129"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="ed140-130">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="ed140-130">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="ed140-131"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ed140-131"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="ed140-132">Il parametro *phReadKey* o *phWriteKey* è null.</span><span class="sxs-lookup"><span data-stu-id="ed140-132">The *phReadKey* or *phWriteKey* parameter is null.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="ed140-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed140-133">Requirements</span></span>



| <span data-ttu-id="ed140-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed140-134">Requirement</span></span> | <span data-ttu-id="ed140-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ed140-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed140-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed140-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ed140-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed140-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ed140-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed140-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ed140-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed140-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ed140-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed140-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed140-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed140-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ed140-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ed140-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed140-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed140-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


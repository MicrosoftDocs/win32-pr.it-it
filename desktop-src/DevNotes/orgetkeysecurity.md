---
description: Recupera una copia del descrittore di sicurezza che protegge la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Funzione ORGetKeySecurity (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330863"
---
# <a name="orgetkeysecurity-function"></a><span data-ttu-id="1c153-103">ORGetKeySecurity (funzione)</span><span class="sxs-lookup"><span data-stu-id="1c153-103">ORGetKeySecurity function</span></span>

<span data-ttu-id="1c153-104">Recupera una copia del descrittore di sicurezza che protegge la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="1c153-104">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c153-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c153-105">Syntax</span></span>


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="1c153-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c153-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c153-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c153-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c153-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="1c153-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="1c153-109">*SecurityInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c153-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c153-110">Valore [delle \_ informazioni di sicurezza](../secauthz/security-information.md) che indica le informazioni di sicurezza richieste.</span><span class="sxs-lookup"><span data-stu-id="1c153-110">A [SECURITY\_INFORMATION](../secauthz/security-information.md) value that indicates the requested security information.</span></span>

</dd> <dt>

<span data-ttu-id="1c153-111">*pSecurityDescriptor* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="1c153-111">*pSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1c153-112">Puntatore a un buffer che riceve una copia del descrittore di sicurezza richiesto.</span><span class="sxs-lookup"><span data-stu-id="1c153-112">A pointer to a buffer that receives a copy of the requested security descriptor.</span></span> <span data-ttu-id="1c153-113">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c153-113">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1c153-114">*lpcbSecurityDescriptor* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1c153-114">*lpcbSecurityDescriptor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c153-115">Puntatore a una variabile che specifica la dimensione, in byte, del buffer a cui punta il parametro *pSecurityDescriptor* .</span><span class="sxs-lookup"><span data-stu-id="1c153-115">A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the *pSecurityDescriptor* parameter.</span></span> <span data-ttu-id="1c153-116">Quando la funzione restituisce, la variabile contiene il numero di byte scritti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="1c153-116">When the function returns, the variable contains the number of bytes written to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c153-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c153-117">Return value</span></span>

<span data-ttu-id="1c153-118">Se la funzione ha esito positivo, la funzione restituisce ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1c153-118">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1c153-119">Se la funzione ha esito negativo, restituisce un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="1c153-119">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="1c153-120">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="1c153-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="1c153-121">Se il buffer specificato dal parametro *pSecurityDescriptor* è troppo piccolo, la funzione restituisce l'errore \_ buffer insufficiente \_ e il parametro *lpcbSecurityDescriptor* contiene il numero di byte necessari per il descrittore di sicurezza richiesto.</span><span class="sxs-lookup"><span data-stu-id="1c153-121">If the buffer specified by the *pSecurityDescriptor* parameter is too small, the function returns ERROR\_INSUFFICIENT\_BUFFER and the *lpcbSecurityDescriptor* parameter contains the number of bytes required for the requested security descriptor.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c153-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c153-122">Requirements</span></span>



| <span data-ttu-id="1c153-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c153-123">Requirement</span></span> | <span data-ttu-id="1c153-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1c153-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c153-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1c153-125">Redistributable</span></span><br/> | <span data-ttu-id="1c153-126">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="1c153-126">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="1c153-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c153-127">Header</span></span><br/>          | <dl> <span data-ttu-id="1c153-128"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c153-128"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c153-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1c153-129">DLL</span></span><br/>             | <dl> <span data-ttu-id="1c153-130"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c153-130"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c153-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c153-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c153-132">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="1c153-132">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="1c153-133">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="1c153-133">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="1c153-134">**ORSetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="1c153-134">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="1c153-135">informazioni di sicurezza \_</span><span class="sxs-lookup"><span data-stu-id="1c153-135">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 

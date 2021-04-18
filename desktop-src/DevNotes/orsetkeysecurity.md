---
description: Imposta la sicurezza di una chiave del registro di sistema aperta in un hive del registro di sistema offline.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Funzione ORSetKeySecurity (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324443"
---
# <a name="orsetkeysecurity-function"></a><span data-ttu-id="9dfc6-103">ORSetKeySecurity (funzione)</span><span class="sxs-lookup"><span data-stu-id="9dfc6-103">ORSetKeySecurity function</span></span>

<span data-ttu-id="9dfc6-104">Imposta la sicurezza di una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="9dfc6-104">Sets the security of an open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dfc6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9dfc6-105">Syntax</span></span>


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="9dfc6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9dfc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dfc6-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dfc6-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dfc6-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="9dfc6-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="9dfc6-109">*SecurityInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dfc6-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dfc6-110">Flag di bit che indicano il tipo di informazioni di sicurezza da impostare.</span><span class="sxs-lookup"><span data-stu-id="9dfc6-110">Bit flags that indicate the type of security information to set.</span></span> <span data-ttu-id="9dfc6-111">Questo parametro può essere una combinazione dei flag di bit per le [ \_ informazioni di sicurezza](../secauthz/security-information.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfc6-111">This parameter can be a combination of the [SECURITY\_INFORMATION](../secauthz/security-information.md) bit flags.</span></span>

</dd> <dt>

<span data-ttu-id="9dfc6-112">*pSecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dfc6-112">*pSecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dfc6-113">Puntatore a una struttura [di \_ descrittori di sicurezza](/windows/win32/api/winnt/ns-winnt-security_descriptor) che specifica gli attributi di sicurezza da impostare per la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="9dfc6-113">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that specifies the security attributes to set for the specified key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dfc6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9dfc6-114">Return value</span></span>

<span data-ttu-id="9dfc6-115">Se la funzione ha esito positivo, la funzione restituisce ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9dfc6-115">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9dfc6-116">Se la funzione ha esito negativo, restituisce un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9dfc6-116">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="9dfc6-117">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="9dfc6-117">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dfc6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dfc6-118">Requirements</span></span>



| <span data-ttu-id="9dfc6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dfc6-119">Requirement</span></span> | <span data-ttu-id="9dfc6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9dfc6-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfc6-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9dfc6-121">Redistributable</span></span><br/> | <span data-ttu-id="9dfc6-122">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="9dfc6-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="9dfc6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dfc6-123">Header</span></span><br/>          | <dl> <span data-ttu-id="9dfc6-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dfc6-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9dfc6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9dfc6-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="9dfc6-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dfc6-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dfc6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dfc6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfc6-128">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="9dfc6-128">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="9dfc6-129">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="9dfc6-129">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="9dfc6-130">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="9dfc6-130">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="9dfc6-131">**ORGetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="9dfc6-131">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="9dfc6-132">descrittore di sicurezza \_</span><span class="sxs-lookup"><span data-stu-id="9dfc6-132">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="9dfc6-133">informazioni di sicurezza \_</span><span class="sxs-lookup"><span data-stu-id="9dfc6-133">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 

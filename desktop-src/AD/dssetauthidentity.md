---
title: Funzione DsSetAuthIdentity (ntdsbcli. h)
description: Imposta il contesto di sicurezza in cui vengono chiamate le API di backup della directory.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsSetAuthIdentity
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477344"
---
# <a name="dssetauthidentity-function"></a><span data-ttu-id="bc221-104">DsSetAuthIdentity (funzione)</span><span class="sxs-lookup"><span data-stu-id="bc221-104">DsSetAuthIdentity function</span></span>

<span data-ttu-id="bc221-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bc221-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bc221-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc221-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bc221-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="bc221-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="bc221-108">La funzione **DsSetAuthIdentity** imposta il contesto di sicurezza in cui vengono chiamate le API di backup della directory.</span><span class="sxs-lookup"><span data-stu-id="bc221-108">The **DsSetAuthIdentity** function sets the security context under which the directory backup APIs are called.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc221-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc221-109">Syntax</span></span>


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a><span data-ttu-id="bc221-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc221-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc221-111">*szUserName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc221-111">*szUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc221-112">Stringa con terminazione null che specifica il nome utente.</span><span class="sxs-lookup"><span data-stu-id="bc221-112">The null-terminated string that specifies the user name.</span></span>

</dd> <dt>

<span data-ttu-id="bc221-113">*szDomainName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc221-113">*szDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc221-114">Stringa con terminazione null che specifica il nome del dominio a cui appartiene l'utente.</span><span class="sxs-lookup"><span data-stu-id="bc221-114">The null-terminated string that specifies the name of the domain that the user belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="bc221-115">*szPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc221-115">*szPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc221-116">Stringa con terminazione null che specifica la password dell'utente nel dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="bc221-116">The null-terminated string that specifies the password of the user in the specified domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc221-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc221-117">Return value</span></span>

<span data-ttu-id="bc221-118">Se l'operazione riesce, restituisce un codice di esito positivo **HRESULT** standard; in caso contrario, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="bc221-118">If successful, returns a standard **HRESULT** success codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc221-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc221-119">Remarks</span></span>

<span data-ttu-id="bc221-120">Se **DsSetAuthIdentity** non viene chiamato, viene utilizzato il contesto di sicurezza del processo corrente.</span><span class="sxs-lookup"><span data-stu-id="bc221-120">If **DsSetAuthIdentity** is not called, security context of the current process is assumed.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc221-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc221-121">Requirements</span></span>



| <span data-ttu-id="bc221-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc221-122">Requirement</span></span> | <span data-ttu-id="bc221-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bc221-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc221-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc221-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc221-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc221-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc221-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc221-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc221-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc221-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc221-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc221-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc221-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc221-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc221-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="bc221-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc221-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc221-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc221-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bc221-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc221-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc221-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc221-134">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bc221-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc221-135">**DsSetAuthIdentityW** (Unicode) e **DsSetAuthIdentityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bc221-135">**DsSetAuthIdentityW** (Unicode) and **DsSetAuthIdentityA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bc221-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc221-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc221-137">Backup e ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="bc221-137">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="bc221-138">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="bc221-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 


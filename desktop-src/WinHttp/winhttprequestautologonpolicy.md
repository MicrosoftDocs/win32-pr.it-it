---
description: Include le impostazioni possibili per i criteri di accesso automatico.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Enumerazione WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307091"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a><span data-ttu-id="02293-103">Enumerazione WinHttpRequestAutoLogonPolicy</span><span class="sxs-lookup"><span data-stu-id="02293-103">WinHttpRequestAutoLogonPolicy enumeration</span></span>

<span data-ttu-id="02293-104">L'enumerazione **WinHttpRequestAutoLogonPolicy** include le possibili impostazioni per il [criterio di accesso automatico](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="02293-104">The **WinHttpRequestAutoLogonPolicy** enumeration includes possible settings for the [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02293-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02293-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a><span data-ttu-id="02293-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="02293-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="02293-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ sempre**</span><span class="sxs-lookup"><span data-stu-id="02293-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy\_Always**</span></span>
</dt> <dd>

<span data-ttu-id="02293-108">Un accesso autenticato, usando le credenziali predefinite, viene eseguito per tutte le richieste.</span><span class="sxs-lookup"><span data-stu-id="02293-108">An authenticated log on, using the default credentials, is performed for all requests.</span></span>

</dd> <dt>

<span data-ttu-id="02293-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**\_OnlyIfBypassProxy AutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="02293-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy\_OnlyIfBypassProxy**</span></span>
</dt> <dd>

<span data-ttu-id="02293-110">Un accesso autenticato, utilizzando le credenziali predefinite, viene eseguito solo per le richieste nella Intranet locale.</span><span class="sxs-lookup"><span data-stu-id="02293-110">An authenticated log on, using the default credentials, is performed only for requests on the local intranet.</span></span> <span data-ttu-id="02293-111">La Intranet locale viene considerata come qualsiasi server nell'elenco proxy bypass nella configurazione del proxy corrente.</span><span class="sxs-lookup"><span data-stu-id="02293-111">The local intranet is considered to be any server on the proxy bypass list in the current proxy configuration.</span></span>

</dd> <dt>

<span data-ttu-id="02293-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ mai**</span><span class="sxs-lookup"><span data-stu-id="02293-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy\_Never**</span></span>
</dt> <dd>

<span data-ttu-id="02293-113">L'autenticazione non viene utilizzata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="02293-113">Authentication is not used automatically.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02293-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="02293-114">Remarks</span></span>

<span data-ttu-id="02293-115">Per impostare i criteri di accesso automatici, chiamare il metodo [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) e specificare una delle costanti precedenti.</span><span class="sxs-lookup"><span data-stu-id="02293-115">To set the automatic logon policy, call the [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) method and specify one of the preceding constants.</span></span>

> [!Note]  
> <span data-ttu-id="02293-116">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="02293-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02293-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02293-117">Requirements</span></span>



| <span data-ttu-id="02293-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="02293-118">Requirement</span></span> | <span data-ttu-id="02293-119">Valore</span><span class="sxs-lookup"><span data-stu-id="02293-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="02293-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02293-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02293-121">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="02293-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="02293-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02293-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02293-123">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="02293-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="02293-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="02293-124">Redistributable</span></span><br/>          | <span data-ttu-id="02293-125">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="02293-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="02293-126">IDL</span><span class="sxs-lookup"><span data-stu-id="02293-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02293-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02293-127"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02293-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02293-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02293-129">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="02293-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 





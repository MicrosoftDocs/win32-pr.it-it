---
description: La struttura UpdateEndpointProxySettings definisce le impostazioni proxy usate per la richiesta di un token.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Struttura UpdateEndpointProxySettings (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049537"
---
# <a name="updateendpointproxysettings-structure"></a><span data-ttu-id="0c60b-103">Struttura UpdateEndpointProxySettings</span><span class="sxs-lookup"><span data-stu-id="0c60b-103">UpdateEndpointProxySettings structure</span></span>

<span data-ttu-id="0c60b-104">La struttura **UpdateEndpointProxySettings** definisce le impostazioni proxy usate per la richiesta di un token.</span><span class="sxs-lookup"><span data-stu-id="0c60b-104">The **UpdateEndpointProxySettings** structure defines the proxy settings used when requesting a token.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c60b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c60b-105">Syntax</span></span>


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a><span data-ttu-id="0c60b-106">Members</span><span class="sxs-lookup"><span data-stu-id="0c60b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c60b-107">**szProxyAddr**</span><span class="sxs-lookup"><span data-stu-id="0c60b-107">**szProxyAddr**</span></span>
</dt> <dd>

<span data-ttu-id="0c60b-108">Il nome DNS o l'indirizzo IP del server proxy da usare (ad esempio, "proxy.somecorp.com" o "192.168.0.4") o una stringa vuota se non è necessario usare un proxy.</span><span class="sxs-lookup"><span data-stu-id="0c60b-108">The DNS name or IP address of the proxy server to use (for example, "proxy.somecorp.com" or "192.168.0.4"), or an empty string if no proxy should be used.</span></span>

</dd> <dt>

<span data-ttu-id="0c60b-109">**szBypassList**</span><span class="sxs-lookup"><span data-stu-id="0c60b-109">**szBypassList**</span></span>
</dt> <dd>

<span data-ttu-id="0c60b-110">Elenco di indirizzi host che devono ignorare il server proxy oppure una stringa vuota se tutti gli indirizzi host devono usare il server proxy</span><span class="sxs-lookup"><span data-stu-id="0c60b-110">A list of host addresses that should bypass the proxy server, or an empty string if all host addresses should use the proxy server</span></span>

<span data-ttu-id="0c60b-111">WUA non utilizza questi dati se **szProxyAddr** è vuoto.</span><span class="sxs-lookup"><span data-stu-id="0c60b-111">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="0c60b-112">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="0c60b-112">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="0c60b-113">Nome utente utilizzato per l'autenticazione con il server proxy oppure stringa vuota se non è necessaria alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0c60b-113">The username that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="0c60b-114">WUA non utilizza questi dati se **szProxyAddr** è vuoto.</span><span class="sxs-lookup"><span data-stu-id="0c60b-114">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="0c60b-115">**szPassword**</span><span class="sxs-lookup"><span data-stu-id="0c60b-115">**szPassword**</span></span>
</dt> <dd>

<span data-ttu-id="0c60b-116">Password utilizzata per l'autenticazione con il server proxy oppure stringa vuota se non è necessaria alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0c60b-116">The password that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="0c60b-117">WUA non utilizza questi dati se **szProxyAddr** è vuoto.</span><span class="sxs-lookup"><span data-stu-id="0c60b-117">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c60b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c60b-118">Requirements</span></span>



| <span data-ttu-id="0c60b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c60b-119">Requirement</span></span> | <span data-ttu-id="0c60b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0c60b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c60b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c60b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c60b-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0c60b-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="0c60b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c60b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c60b-124">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0c60b-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0c60b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c60b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c60b-126"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c60b-126"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c60b-127">IDL</span><span class="sxs-lookup"><span data-stu-id="0c60b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c60b-128"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c60b-128"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c60b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c60b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c60b-130">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="0c60b-130">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 





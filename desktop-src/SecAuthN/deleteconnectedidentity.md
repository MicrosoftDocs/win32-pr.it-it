---
description: Elimina le credenziali utente usate per l'identità connessa.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Funzione DeleteConnectedIdentity (Indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049366"
---
# <a name="deleteconnectedidentity-function"></a><span data-ttu-id="5d55a-103">DeleteConnectedIdentity (funzione)</span><span class="sxs-lookup"><span data-stu-id="5d55a-103">DeleteConnectedIdentity function</span></span>

<span data-ttu-id="5d55a-104">Elimina le credenziali utente usate per l'identità connessa.</span><span class="sxs-lookup"><span data-stu-id="5d55a-104">Deletes the user credential used for the connected identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d55a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d55a-105">Syntax</span></span>


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a><span data-ttu-id="5d55a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d55a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d55a-107">*ProviderHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d55a-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d55a-108">Handle del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="5d55a-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="5d55a-109">*UserToken* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5d55a-109">*UserToken* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d55a-110">Token dell'utente connesso il cui account verrà convertito in un account locale.</span><span class="sxs-lookup"><span data-stu-id="5d55a-110">Token of the connected user whose account is going to be converted to a local account.</span></span> <span data-ttu-id="5d55a-111">Se *userToken* non è **null**, il provider di identità utilizza questo token per caricare il profilo utente e pulire gli stati connessi.</span><span class="sxs-lookup"><span data-stu-id="5d55a-111">If *UserToken* is not **NULL**, the identity provider uses this token to load the user profile and clean up connected states.</span></span> <span data-ttu-id="5d55a-112">Se *userToken* è **null**, LSA forza la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="5d55a-112">If *UserToken* is **NULL**, LSA is forcing the disconnection.</span></span> <span data-ttu-id="5d55a-113">Il provider di identità deve pulire tutti gli stati connessi globali per questo utente, ma non è necessario che il provider ripulisca gli stati connessi nel profilo utente.</span><span class="sxs-lookup"><span data-stu-id="5d55a-113">The identity provider should clean up any global connected states on this user, but the provider does not have to clean up connected states in the user profile.</span></span>

</dd> <dt>

<span data-ttu-id="5d55a-114">*UserSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d55a-114">*UserSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d55a-115">SID primario dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="5d55a-115">The primary SID of the connected user.</span></span> <span data-ttu-id="5d55a-116">Se *userToken* non è **null**, questo parametro è il SID utente del token.</span><span class="sxs-lookup"><span data-stu-id="5d55a-116">If *UserToken* is not **NULL**, this parameter is the user SID of the token.</span></span> <span data-ttu-id="5d55a-117">Se *userToken* è **null**, questo parametro viene usato per identificare l'utente connesso e pulire gli Stati di connessione globale di tale utente.</span><span class="sxs-lookup"><span data-stu-id="5d55a-117">If *UserToken* is **NULL**, this parameter is used to identify the connected user and clean up global connected states of that user.</span></span>

</dd> <dt>

<span data-ttu-id="5d55a-118">*IdentityUserName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d55a-118">*IdentityUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d55a-119">Nome utente dell'identità.</span><span class="sxs-lookup"><span data-stu-id="5d55a-119">The user name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d55a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d55a-120">Return value</span></span>

<span data-ttu-id="5d55a-121">Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5d55a-121">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="5d55a-122">Se la funzione ha esito negativo, la funzione può restituire uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="5d55a-122">If the function fails, the function may return one of the following error codes.</span></span>



| <span data-ttu-id="5d55a-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d55a-123">Return value</span></span>                                                                                               | <span data-ttu-id="5d55a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d55a-124">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d55a-125"><dt>STATO \_ parametro non valido \_</dt></span><span class="sxs-lookup"><span data-stu-id="5d55a-125"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>      | <span data-ttu-id="5d55a-126">Un parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="5d55a-126">A parameter is not valid.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="5d55a-127"><dt>STATO \_ senza \_ tale \_ utente</dt></span><span class="sxs-lookup"><span data-stu-id="5d55a-127"><dt>STATUS\_NO\_SUCH\_USER</dt></span></span> </dl>          | <span data-ttu-id="5d55a-128">L'utente identificato da *UserSID* non esiste, non è attualmente connesso o non esiste alcuna identità il cui nome utente corrisponde a *IdentityUserName*.</span><span class="sxs-lookup"><span data-stu-id="5d55a-128">The user identified by *UserSid* does not exist, is not currently connected, or there is no identity whose user name matches *IdentityUserName*.</span></span><br/> |
| <dl> <span data-ttu-id="5d55a-129"><dt>STATO \_ risorse insufficienti \_</dt></span><span class="sxs-lookup"><span data-stu-id="5d55a-129"><dt>STATUS\_INSUFFICIENT\_RESOURCES</dt></span></span> </dl> | <span data-ttu-id="5d55a-130">Memoria insufficiente per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5d55a-130">There is not enough memory to process the request.</span></span><br/>                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="5d55a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d55a-131">Requirements</span></span>



| <span data-ttu-id="5d55a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d55a-132">Requirement</span></span> | <span data-ttu-id="5d55a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5d55a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d55a-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d55a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5d55a-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5d55a-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="5d55a-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d55a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5d55a-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5d55a-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d55a-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d55a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d55a-139"><dt>Indentitystore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d55a-139"><dt>Indentitystore.h</dt></span></span> </dl> |



 

 





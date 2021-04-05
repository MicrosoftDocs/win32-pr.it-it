---
description: Verifica che il profilo utente online sia caricato.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Funzione OnProfileLoaded (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756434"
---
# <a name="onprofileloaded-function"></a><span data-ttu-id="99428-103">OnProfileLoaded (funzione)</span><span class="sxs-lookup"><span data-stu-id="99428-103">OnProfileLoaded function</span></span>

<span data-ttu-id="99428-104">Verifica che il profilo utente online sia caricato.</span><span class="sxs-lookup"><span data-stu-id="99428-104">Checks that the online user profile is loaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="99428-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99428-105">Syntax</span></span>


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a><span data-ttu-id="99428-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99428-107">*ProviderHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99428-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99428-108">Handle del provider.</span><span class="sxs-lookup"><span data-stu-id="99428-108">The provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="99428-109">*UserToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99428-109">*UserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99428-110">Token dell'utente di cui è in corso il caricamento o lo scaricamento del profilo.</span><span class="sxs-lookup"><span data-stu-id="99428-110">Token of the user whose profile is being loaded or unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="99428-111">Con *caricamento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99428-111">*Loaded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99428-112">**True** se il profilo è stato caricato.</span><span class="sxs-lookup"><span data-stu-id="99428-112">**TRUE** if the profile has been loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99428-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99428-113">Return value</span></span>

<span data-ttu-id="99428-114">Se la funzione ha esito positivo, la funzione restituisce lo stato \_ Success.</span><span class="sxs-lookup"><span data-stu-id="99428-114">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="99428-115">Se la funzione ha esito negativo, la funzione restituisce un codice di errore diverso da zero che è un errore specifico del provider a scopo diagnostico.</span><span class="sxs-lookup"><span data-stu-id="99428-115">If the function fails, the function returns a nonzero error code that is a provider-specific error for diagnostic purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="99428-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="99428-116">Remarks</span></span>

<span data-ttu-id="99428-117">Questa funzione viene chiamata ogni volta che viene chiamata la funzione [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="99428-117">This function is called each time the [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) function is called.</span></span> <span data-ttu-id="99428-118">Non è sincronizzato con **LoadUserProfile**; ovvero è possibile che sia stato restituito **LoadUserProfile** e che il profilo sia stato scaricato dal momento in cui è stata chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="99428-118">It is not synchronized with **LoadUserProfile**; that is, **LoadUserProfile** might have returned and the profile might have been unloaded by the time the function was called.</span></span> <span data-ttu-id="99428-119">Questa funzione può essere chiamata più volte anche quando il profilo è stato caricato.</span><span class="sxs-lookup"><span data-stu-id="99428-119">This function can be called more than once even when the profile has been loaded.</span></span> <span data-ttu-id="99428-120">Il provider di identità non deve presupporre che una chiamata a questa funzione con *Loaded* uguale a true sarà seguita da una chiamata con *Loaded* uguale a false.</span><span class="sxs-lookup"><span data-stu-id="99428-120">The identity provider must not assume that a call to this function with *Loaded* equal to TRUE will be followed by a call with *Loaded* equal to FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="99428-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99428-121">Requirements</span></span>



| <span data-ttu-id="99428-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="99428-122">Requirement</span></span> | <span data-ttu-id="99428-123">Valore</span><span class="sxs-lookup"><span data-stu-id="99428-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99428-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99428-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99428-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="99428-125">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="99428-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99428-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99428-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="99428-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99428-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99428-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="99428-129"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="99428-129"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

 

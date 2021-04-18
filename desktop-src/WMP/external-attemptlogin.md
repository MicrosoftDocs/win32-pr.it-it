---
title: External. attemptLogin, metodo
description: Il metodo attemptLogin Visualizza una finestra di dialogo in modo che l'utente possa tentare di accedere al negozio online.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Metodo attemptLogin Windows Media Player
- Metodo attemptLogin Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328412"
---
# <a name="externalattemptlogin-method"></a><span data-ttu-id="02f45-106">External. attemptLogin, metodo</span><span class="sxs-lookup"><span data-stu-id="02f45-106">External.attemptLogin method</span></span>

<span data-ttu-id="02f45-107">Il metodo **attemptLogin** Visualizza una finestra di dialogo in modo che l'utente possa tentare di accedere al negozio online.</span><span class="sxs-lookup"><span data-stu-id="02f45-107">The **attemptLogin** method displays a dialog box so the user can attempt to log in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f45-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02f45-108">Syntax</span></span>


```JScript
External.attemptLogin()
```



## <a name="parameters"></a><span data-ttu-id="02f45-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="02f45-109">Parameters</span></span>

<span data-ttu-id="02f45-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="02f45-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02f45-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02f45-111">Return value</span></span>

<span data-ttu-id="02f45-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="02f45-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f45-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="02f45-113">Remarks</span></span>

<span data-ttu-id="02f45-114">Se il tentativo di accesso comporta una modifica dello stato di accesso, Windows Media Player genera l'evento [OnLoginChange](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="02f45-114">If the log-in attempt results in a change of log-in status, Windows Media Player raises the [OnLoginChange](external-onloginchange-event.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f45-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02f45-115">Requirements</span></span>



| <span data-ttu-id="02f45-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="02f45-116">Requirement</span></span> | <span data-ttu-id="02f45-117">Valore</span><span class="sxs-lookup"><span data-stu-id="02f45-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02f45-118">Versione</span><span class="sxs-lookup"><span data-stu-id="02f45-118">Version</span></span><br/> | <span data-ttu-id="02f45-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="02f45-119">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="02f45-120">DLL</span><span class="sxs-lookup"><span data-stu-id="02f45-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="02f45-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02f45-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02f45-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02f45-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f45-123">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="02f45-123">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="02f45-124">**Evento External. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="02f45-124">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="02f45-125">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="02f45-125">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="02f45-126">**IWMPContentPartner:: login**</span><span class="sxs-lookup"><span data-stu-id="02f45-126">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="02f45-127">**Gestione dell'accesso**</span><span class="sxs-lookup"><span data-stu-id="02f45-127">**Managing Login**</span></span>](managing-login.md)
</dt> </dl>

 

 






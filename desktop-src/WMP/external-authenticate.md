---
title: External. Authenticate (metodo)
description: Il metodo Authenticate avvia un tentativo di autenticazione dell'utente.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- Metodo di autenticazione Media Player Windows
- metodo Authenticate Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo Authenticate
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328411"
---
# <a name="externalauthenticate-method"></a><span data-ttu-id="66813-106">External. Authenticate (metodo)</span><span class="sxs-lookup"><span data-stu-id="66813-106">External.authenticate method</span></span>

<span data-ttu-id="66813-107">Il metodo **Authenticate** avvia un tentativo di autenticazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66813-107">The **authenticate** method initiates an attempt to authenticate the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="66813-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66813-108">Syntax</span></span>


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a><span data-ttu-id="66813-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="66813-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66813-110">*AuthenticationIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66813-110">*AuthenticationIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66813-111">**Numero** (**Long**) che specifica l'indice di una pagina Web di autenticazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="66813-111">**Number** (**long**) that specifies the index of an authentication-success webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66813-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66813-112">Return value</span></span>

<span data-ttu-id="66813-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="66813-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66813-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="66813-114">Remarks</span></span>

<span data-ttu-id="66813-115">Alcuni collegamenti in una pagina di individuazione hanno destinazioni che devono essere visualizzate solo dopo che l'utente è stato autenticato.</span><span class="sxs-lookup"><span data-stu-id="66813-115">Certain links on a discovery page have targets that should be displayed only after the user has been authenticated.</span></span> <span data-ttu-id="66813-116">La pagina di individuazione, Windows Media Player e il plug-in Online Store usano la procedura seguente per autenticare l'utente e visualizzare la pagina Web di destinazione:</span><span class="sxs-lookup"><span data-stu-id="66813-116">The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:</span></span>

1.  <span data-ttu-id="66813-117">Script in una pagina di individuazione chiama l'oggetto *esterno*. metodo **Authenticate** .</span><span class="sxs-lookup"><span data-stu-id="66813-117">Script on a discovery page calls the *External*.**authenticate** method.</span></span>
2.  <span data-ttu-id="66813-118">Windows Media Player visualizza una finestra di dialogo per ottenere un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="66813-118">Windows Media Player displays a dialog box to obtain a user name and password.</span></span>
3.  <span data-ttu-id="66813-119">Windows Media Player chiama [IWMPContentPartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), che avvia il tentativo di autenticazione e restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="66813-119">Windows Media Player calls [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), which initiates the authentication attempt and returns immediately.</span></span>
4.  <span data-ttu-id="66813-120">Al termine del tentativo di autenticazione, il plug-in Online Store chiama [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnAuthResult e un valore booleano che indica se il tentativo ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="66813-120">When the authentication attempt is complete, the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</span></span>
5.  <span data-ttu-id="66813-121">Se il tentativo di autenticazione ha avuto esito positivo, Windows Media Player chiama [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ AuthenticationSuccessURL, per ottenere l'URL di una pagina Web di autenticazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="66813-121">If the authentication attempt was successful, Windows Media Player calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage.</span></span> <span data-ttu-id="66813-122">In questa chiamata, Windows Media Player passa lo stesso indice che la pagina di individuazione passa a *External*. metodo **Authenticate** .</span><span class="sxs-lookup"><span data-stu-id="66813-122">In this call, Windows Media Player passes the same index that the discovery page passed to the *External*.**authenticate** method.</span></span>
6.  <span data-ttu-id="66813-123">Windows Media Player Visualizza la pagina Web autenticazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="66813-123">Windows Media Player displays the authentication-success webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="66813-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66813-124">Requirements</span></span>



| <span data-ttu-id="66813-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="66813-125">Requirement</span></span> | <span data-ttu-id="66813-126">Valore</span><span class="sxs-lookup"><span data-stu-id="66813-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66813-127">Versione</span><span class="sxs-lookup"><span data-stu-id="66813-127">Version</span></span><br/> | <span data-ttu-id="66813-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="66813-128">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="66813-129">DLL</span><span class="sxs-lookup"><span data-stu-id="66813-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="66813-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66813-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66813-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66813-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66813-132">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="66813-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="66813-133">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="66813-133">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="66813-134">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="66813-134">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 






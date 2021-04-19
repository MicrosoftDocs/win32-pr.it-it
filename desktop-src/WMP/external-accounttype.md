---
title: External. accountType
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà accountType Recupera il tipo di account dell'utente corrente.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Media Player di Windows External. accountType
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329933"
---
# <a name="externalaccounttype"></a><span data-ttu-id="4f5bd-106">External. accountType</span><span class="sxs-lookup"><span data-stu-id="4f5bd-106">External.accountType</span></span>

> [!Note]  
> <span data-ttu-id="4f5bd-107">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4f5bd-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4f5bd-109">La proprietà **AccountType** Recupera il tipo di account dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-109">The **accountType** property retrieves the account type of the current user.</span></span>

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a><span data-ttu-id="4f5bd-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="4f5bd-110">Possible Values</span></span>

<span data-ttu-id="4f5bd-111">Questa proprietà è una **stringa** di sola lettura che rappresenta il tipo di conto.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-111">This property is a read-only **String** that represents the account type.</span></span> <span data-ttu-id="4f5bd-112">Le stringhe che rappresentano i diversi tipi di conto sono definite dall'archivio online.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-112">Strings that represent various account types are defined by the online store.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5bd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f5bd-113">Remarks</span></span>

<span data-ttu-id="4f5bd-114">Questa proprietà recupera il tipo di conto chiamando il metodo [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , che viene implementato dal plug-in del negozio online.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-114">This property retrieves the account type by calling the [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="4f5bd-115">Se l'utente corrente è connesso allo Store online oppure il plug-in ha memorizzato nella cache le credenziali dell'utente, il metodo **getContentPartnerInfo** può determinare il tipo di account dell'utente e restituirlo a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-115">If the current user is logged in to the online store or the plug-in has cached the user's credentials, the **getContentPartnerInfo** method can determine the user's account type and return it to Windows Media Player.</span></span> <span data-ttu-id="4f5bd-116">Il tipo di account è una stringa che Windows Media Player non interpreta.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-116">The account type is a string that Windows Media Player does not interpret.</span></span> <span data-ttu-id="4f5bd-117">Windows Media Player invece passa la stringa dal plug-in Online Store allo script nella pagina di individuazione del negozio online.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-117">Rather, Windows Media Player passes the string from the online store's plug-in to the script on the online store's discovery page.</span></span>

<span data-ttu-id="4f5bd-118">Se l'utente corrente non è connesso allo Store online e il plug-in del negozio online non dispone di credenziali memorizzate nella cache per l'utente, questa proprietà recupera qualsiasi stringa restituita dal metodo **getContentPartnerInfo** in tale situazione.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-118">If the current user is not logged in to the online store and the online store's plug-in does not have cached credentials for the user, this property retrieves whatever string the **getContentPartnerInfo** method returns in that situation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5bd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f5bd-119">Requirements</span></span>



| <span data-ttu-id="4f5bd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f5bd-120">Requirement</span></span> | <span data-ttu-id="4f5bd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4f5bd-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5bd-122">Versione</span><span class="sxs-lookup"><span data-stu-id="4f5bd-122">Version</span></span><br/> | <span data-ttu-id="4f5bd-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="4f5bd-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="4f5bd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4f5bd-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f5bd-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f5bd-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f5bd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f5bd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5bd-127">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="4f5bd-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4f5bd-128">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="4f5bd-128">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 






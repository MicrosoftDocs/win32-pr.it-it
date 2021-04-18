---
title: External. userLoggedIn
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. userLoggedIn
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- Media Player di Windows External. userLoggedIn
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328405"
---
# <a name="externaluserloggedin"></a><span data-ttu-id="d8834-105">External. userLoggedIn</span><span class="sxs-lookup"><span data-stu-id="d8834-105">External.userLoggedIn</span></span>

> [!Note]  
> <span data-ttu-id="d8834-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="d8834-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d8834-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d8834-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d8834-108">La proprietà **userLoggedIn** recupera un valore che indica se l'utente è connesso al negozio online.</span><span class="sxs-lookup"><span data-stu-id="d8834-108">The **userLoggedIn** property retrieves a value indicating whether the user is logged in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8834-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8834-109">Syntax</span></span>

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a><span data-ttu-id="d8834-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d8834-110">Possible Values</span></span>

<span data-ttu-id="d8834-111">Questa proprietà è un **valore booleano** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d8834-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="d8834-112">**True** indica che l'utente è connesso e **false** indica che l'utente è stato disconnesso.</span><span class="sxs-lookup"><span data-stu-id="d8834-112">**TRUE** indicates that the user is logged in, and **FALSE** indicates that the user is logged out.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8834-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8834-113">Requirements</span></span>



| <span data-ttu-id="d8834-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8834-114">Requirement</span></span> | <span data-ttu-id="d8834-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d8834-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8834-116">Versione</span><span class="sxs-lookup"><span data-stu-id="d8834-116">Version</span></span><br/> | <span data-ttu-id="d8834-117">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d8834-117">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="d8834-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d8834-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8834-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8834-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8834-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8834-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8834-121">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="d8834-121">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d8834-122">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="d8834-122">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="d8834-123">**Evento External. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="d8834-123">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> </dl>

 

 






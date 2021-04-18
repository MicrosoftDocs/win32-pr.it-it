---
description: Costante numerica che specifica il numero massimo di caratteri che alcuni provider di crittografia Microsoft utilizzeranno per ottenere l'ID utente.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: MAXUIDLEN (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307691"
---
# <a name="maxuidlen"></a><span data-ttu-id="9caff-103">MAXUIDLEN</span><span class="sxs-lookup"><span data-stu-id="9caff-103">MAXUIDLEN</span></span>

<span data-ttu-id="9caff-104">MAXUIDLEN è una costante numerica che specifica il numero massimo di caratteri che alcuni provider di crittografia Microsoft utilizzeranno per ottenere l'ID utente. MAXUIDLEN è definito in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="9caff-104">MAXUIDLEN is a numeric constant that specifies the maximum number of characters that some of the Microsoft cryptographic providers will use when obtaining the user ID.MAXUIDLEN is defined in Wincrypt.h.</span></span>



| <span data-ttu-id="9caff-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="9caff-105">Constant/value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="9caff-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9caff-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <span data-ttu-id="9caff-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="9caff-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span></span> </dl> | <span data-ttu-id="9caff-108">Quando il parametro *pszContainer* della funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) è **null**, alcuni provider di servizi di crittografia Microsoft usano il nome di accesso dell'utente attualmente connesso come nome del contenitore di chiavi.</span><span class="sxs-lookup"><span data-stu-id="9caff-108">When the *pszContainer* parameter of the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function is **NULL**, some of the Microsoft cryptographic providers use the logon name of the currently logged on user as the key container name.</span></span> <span data-ttu-id="9caff-109">MAXUIDLEN specifica il numero massimo di caratteri, incluso il carattere **null** di terminazione, che questi provider utilizzeranno per il nome utente.</span><span class="sxs-lookup"><span data-stu-id="9caff-109">MAXUIDLEN specifies the maximum number of characters, including the terminating **NULL** character, that these providers will use for the user name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9caff-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9caff-110">Requirements</span></span>



| <span data-ttu-id="9caff-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9caff-111">Requirement</span></span> | <span data-ttu-id="9caff-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9caff-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9caff-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9caff-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9caff-114">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9caff-114">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9caff-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9caff-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9caff-116">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9caff-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9caff-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9caff-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9caff-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="9caff-118"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9caff-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9caff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9caff-120">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="9caff-120">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[<span data-ttu-id="9caff-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="9caff-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 





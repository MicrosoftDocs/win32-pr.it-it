---
description: "Il \\_ \\_ tipo di dati dell'handle di enumerazione LSA viene usato dalla funzione LSA che enumera gli oggetti trustedDomain: LsaEnumerateTrustedDomainsEx."
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312770"
---
# <a name="lsa_enumeration_handle"></a><span data-ttu-id="f11f7-103">\_handle di enumerazione LSA \_</span><span class="sxs-lookup"><span data-stu-id="f11f7-103">LSA\_ENUMERATION\_HANDLE</span></span>

<span data-ttu-id="f11f7-104">Il tipo di dati dell' **\_ \_ handle di enumerazione LSA** viene usato dalla funzione LSA che enumera gli oggetti [**trustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="f11f7-104">The **LSA\_ENUMERATION\_HANDLE** data type is used by the LSA function that enumerates [**TrustedDomain**](trusteddomain-object.md) objects: [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span> <span data-ttu-id="f11f7-105">Questa funzione è progettata in modo da poter effettuare più chiamate per enumerare tutti gli oggetti di un determinato tipo nel database.</span><span class="sxs-lookup"><span data-stu-id="f11f7-105">This function is designed so that you can make multiple calls to enumerate all the objects of a given type in the database.</span></span>

<span data-ttu-id="f11f7-106">Nella chiamata di funzione di enumerazione iniziale si passa un puntatore a una variabile **dell' \_ \_ handle di enumerazione LSA** inizializzata su zero.</span><span class="sxs-lookup"><span data-stu-id="f11f7-106">On the initial enumeration function call, you pass in a pointer to an **LSA\_ENUMERATION\_HANDLE** variable that is initialized to zero.</span></span> <span data-ttu-id="f11f7-107">La funzione aggiorna questo valore.</span><span class="sxs-lookup"><span data-stu-id="f11f7-107">The function updates this value.</span></span> <span data-ttu-id="f11f7-108">Se la funzione restituisce un valore che indica la presenza di più oggetti da enumerare, chiamare di nuovo la funzione e passare il valore dell' **\_ \_ handle di enumerazione LSA** aggiornato per ottenere un'enumerazione continua dal punto in cui l'enumerazione precedente è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="f11f7-108">If the function returns a value that indicates there are more objects to enumerate, call the function again and pass in the updated **LSA\_ENUMERATION\_HANDLE** value to obtain an enumeration continuing from the point where the previous enumeration left off.</span></span>


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="f11f7-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f11f7-109">Requirements</span></span>



| <span data-ttu-id="f11f7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f11f7-110">Requirement</span></span> | <span data-ttu-id="f11f7-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f11f7-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f11f7-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f11f7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f11f7-113">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f11f7-113">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f11f7-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f11f7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f11f7-115">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f11f7-115">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f11f7-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f11f7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f11f7-117"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f11f7-117"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f11f7-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f11f7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11f7-119">**LsaEnumerateTrustedDomainsEx**</span><span class="sxs-lookup"><span data-stu-id="f11f7-119">**LsaEnumerateTrustedDomainsEx**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 





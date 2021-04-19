---
description: Aggiunge un nome di rete locale alternativo per il computer da cui viene chiamato.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331204"
---
# <a name="addlocalalternatecomputername-function"></a><span data-ttu-id="85a6f-103">AddLocalAlternateComputerName (funzione)</span><span class="sxs-lookup"><span data-stu-id="85a6f-103">AddLocalAlternateComputerName function</span></span>

<span data-ttu-id="85a6f-104">Aggiunge un nome di rete locale alternativo per il computer da cui viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="85a6f-104">Adds an alternate local network name for the computer from which it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a6f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85a6f-105">Syntax</span></span>


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="85a6f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85a6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a6f-107">*lpDnsFQHostname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85a6f-107">*lpDnsFQHostname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a6f-108">Nome alternativo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="85a6f-108">The alternate name to be added.</span></span> <span data-ttu-id="85a6f-109">Il nome deve essere nel formato **ComputerNameDnsFullyQualified** come definito nell'enumerazione del [**\_ \_ formato del nome del computer**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) e la funzione [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) deve essere in grado di convalidarla con il formato impostato su **DnsNameHostnameFull**.</span><span class="sxs-lookup"><span data-stu-id="85a6f-109">The name must be in the **ComputerNameDnsFullyQualified** format as defined in the [**COMPUTER\_NAME\_FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) enumeration, and the [**DnsValidateName\_W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) function must be able to validate it with its format set to **DnsNameHostnameFull**.</span></span>

</dd> <dt>

<span data-ttu-id="85a6f-110">*ulFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85a6f-110">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a6f-111">Questo parametro è riservato e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="85a6f-111">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a6f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85a6f-112">Return value</span></span>

<span data-ttu-id="85a6f-113">Se la funzione ha esito positivo, la funzione restituisce **Error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="85a6f-113">If the function succeeds, the function returns **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="85a6f-114">Se la funzione ha esito negativo, viene restituito un codice di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="85a6f-114">If the function fails, it returns a nonzero error code.</span></span> <span data-ttu-id="85a6f-115">Tra i codici di errore restituiti sono inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="85a6f-115">Among the error codes that it returns are the following:</span></span>



| <span data-ttu-id="85a6f-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="85a6f-116">Return code</span></span>                                                                                               | <span data-ttu-id="85a6f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85a6f-117">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85a6f-118"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85a6f-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="85a6f-119">Indica che il parametro *lpDnsFQHostname* non punta a un nome DNS valido o che il parametro *ulFlags* non è uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="85a6f-119">Indicates that the *lpDnsFQHostname* parameter does not point to a valid DNS name, or that the *ulFlags* parameter is not equal to zero.</span></span><br/> |
| <dl> <span data-ttu-id="85a6f-120"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85a6f-120"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="85a6f-121">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="85a6f-121">There is not enough memory to complete the operation.</span></span><br/>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="85a6f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85a6f-122">Requirements</span></span>



| <span data-ttu-id="85a6f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="85a6f-123">Requirement</span></span> | <span data-ttu-id="85a6f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="85a6f-124">Value</span></span> |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85a6f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="85a6f-125">Library</span></span><br/>                | <dl> <span data-ttu-id="85a6f-126"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="85a6f-126"><dt>Kernel32.lib</dt></span></span> </dl>               |
| <span data-ttu-id="85a6f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="85a6f-127">DLL</span></span><br/>                    | <dl> <span data-ttu-id="85a6f-128"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85a6f-128"><dt>Kernel32.dll</dt></span></span> </dl>               |
| <span data-ttu-id="85a6f-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="85a6f-129">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="85a6f-130">**AddLocalAlternateComputerNameW** (Unicode) e **AddLocalAlternateComputerNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="85a6f-130">**AddLocalAlternateComputerNameW** (Unicode) and **AddLocalAlternateComputerNameA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85a6f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85a6f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a6f-132">**\_formato nome \_ computer**</span><span class="sxs-lookup"><span data-stu-id="85a6f-132">**COMPUTER\_NAME\_FORMAT**</span></span>](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[<span data-ttu-id="85a6f-133">**DnsValidateName \_ W**</span><span class="sxs-lookup"><span data-stu-id="85a6f-133">**DnsValidateName\_W**</span></span>](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 

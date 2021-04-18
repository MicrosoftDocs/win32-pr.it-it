---
description: Rappresenta le factory di attivazione registrate chiamando la funzione RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307063"
---
# <a name="ro_registration_cookie"></a><span data-ttu-id="346c0-103">\_cookie di registrazione ro \_</span><span class="sxs-lookup"><span data-stu-id="346c0-103">RO\_REGISTRATION\_COOKIE</span></span>

<span data-ttu-id="346c0-104">Rappresenta le factory di attivazione registrate chiamando la funzione [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .</span><span class="sxs-lookup"><span data-stu-id="346c0-104">Represents activation factories that are registered by calling the [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function.</span></span>


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a><span data-ttu-id="346c0-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="346c0-105">Remarks</span></span>

<span data-ttu-id="346c0-106">La funzione [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) restituisce un **\_ \_ cookie di registrazione ro** quando un attivabile class factory viene registrato con la Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="346c0-106">The [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function returns a **RO\_REGISTRATION\_COOKIE** when a activatable class factories are registered with the Windows Runtime.</span></span> <span data-ttu-id="346c0-107">La funzione [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa il cookie per rimuovere le class factory.</span><span class="sxs-lookup"><span data-stu-id="346c0-107">The [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) function uses the cookie to remove the class factories.</span></span>

## <a name="requirements"></a><span data-ttu-id="346c0-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="346c0-108">Requirements</span></span>



| <span data-ttu-id="346c0-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="346c0-109">Requirement</span></span> | <span data-ttu-id="346c0-110">Valore</span><span class="sxs-lookup"><span data-stu-id="346c0-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="346c0-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="346c0-111">Minimum supported client</span></span><br/> | <span data-ttu-id="346c0-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="346c0-112">Windows 8</span></span><br/>                                                               |
| <span data-ttu-id="346c0-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="346c0-113">Minimum supported server</span></span><br/> | <span data-ttu-id="346c0-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="346c0-114">Windows Server 2012</span></span><br/>                                                     |
| <span data-ttu-id="346c0-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="346c0-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="346c0-116"><dt>Roapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="346c0-116"><dt>Roapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346c0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="346c0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346c0-118">**RoRegisterActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="346c0-118">**RoRegisterActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[<span data-ttu-id="346c0-119">**RoRevokeActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="346c0-119">**RoRevokeActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 

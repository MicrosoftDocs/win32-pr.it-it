---
description: La definizione dell'interfaccia ISCardAuth viene fornita come standard che può essere seguita durante lo sviluppo di un provider di servizi per smart card. L'interfaccia ISCardAuth può essere usata per esporre i servizi di autenticazione supportati da una smart card.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interfaccia ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484724"
---
# <a name="iscardauth-interface"></a><span data-ttu-id="78a11-103">Interfaccia ISCardAuth</span><span class="sxs-lookup"><span data-stu-id="78a11-103">ISCardAuth interface</span></span>

<span data-ttu-id="78a11-104">\[L'interfaccia **ISCardAuth** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="78a11-104">\[The **ISCardAuth** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="78a11-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="78a11-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="78a11-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="78a11-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="78a11-107">La definizione dell'interfaccia **ISCardAuth** viene fornita come standard che può essere seguita durante lo sviluppo di un [*provider di servizi*](../secgloss/c-gly.md)per [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="78a11-107">The **ISCardAuth** interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="78a11-108">L'interfaccia **ISCardAuth** può essere usata per esporre i servizi di autenticazione supportati da una smart card.</span><span class="sxs-lookup"><span data-stu-id="78a11-108">The **ISCardAuth** interface can be used to expose authentication services supported by a smart card.</span></span> <span data-ttu-id="78a11-109">Questi servizi includono l'autenticazione dell'applicazione, l'autenticazione con smart card e l'autenticazione utente.</span><span class="sxs-lookup"><span data-stu-id="78a11-109">These services include application authentication, smart card authentication, and user authentication.</span></span>

<span data-ttu-id="78a11-110">Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="78a11-110">The following example shows a typical use of the **ISCardAuth** interface.</span></span>

<span data-ttu-id="78a11-111">**Per usare ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="78a11-111">**To use ISCardAuth**</span></span>

1.  <span data-ttu-id="78a11-112">Creare un'interfaccia **ISCardAuth** (tramite il metodo di interfaccia [**ISCardManage**](iscardmanage.md) corrispondente).</span><span class="sxs-lookup"><span data-stu-id="78a11-112">Create an **ISCardAuth** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="78a11-113">Chiamare il metodo **ISCardAuth** appropriato ([**\_ autenticazione app**](iscardauth-app-auth.md), [**getchallenge**](iscardauth-getchallenge.md), [**CPI \_ AUTH**](iscardauth-icc-auth.md)o [**\_ autenticazione utente**](iscardauth-user-auth.md)).</span><span class="sxs-lookup"><span data-stu-id="78a11-113">Call the appropriate **ISCardAuth** method ([**APP\_Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC\_Auth**](iscardauth-icc-auth.md), or [**User\_Auth**](iscardauth-user-auth.md)).</span></span>
3.  <span data-ttu-id="78a11-114">Rilasciare l'interfaccia **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="78a11-114">Release the **ISCardAuth** interface.</span></span>

## <a name="members"></a><span data-ttu-id="78a11-115">Membri</span><span class="sxs-lookup"><span data-stu-id="78a11-115">Members</span></span>

<span data-ttu-id="78a11-116">L'interfaccia **ISCardAuth** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="78a11-116">The **ISCardAuth** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="78a11-117">**ISCardAuth** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="78a11-117">**ISCardAuth** also has these types of members:</span></span>

-   [<span data-ttu-id="78a11-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="78a11-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="78a11-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="78a11-119">Methods</span></span>

<span data-ttu-id="78a11-120">L'interfaccia **ISCardAuth** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="78a11-120">The **ISCardAuth** interface has these methods.</span></span>



| <span data-ttu-id="78a11-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="78a11-121">Method</span></span>                                          | <span data-ttu-id="78a11-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78a11-122">Description</span></span>                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78a11-123">**Autenticazione dell'APP \_**</span><span class="sxs-lookup"><span data-stu-id="78a11-123">**APP\_Auth**</span></span>](iscardauth-app-auth.md)        | <span data-ttu-id="78a11-124">Consente all'applicazione di eseguire l'autenticazione usando un protocollo di verifica/firma.</span><span class="sxs-lookup"><span data-stu-id="78a11-124">Allows the application to authenticate itself using a challenge/signature protocol.</span></span><br/> |
| [<span data-ttu-id="78a11-125">**Getchallenge**</span><span class="sxs-lookup"><span data-stu-id="78a11-125">**GetChallenge**</span></span>](iscardauth-getchallenge.md) | <span data-ttu-id="78a11-126">Restituisce una richiesta di verifica dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="78a11-126">Returns a challenge from the smart card.</span></span><br/>                                            |
| [<span data-ttu-id="78a11-127">**\_Autenticazione ICC**</span><span class="sxs-lookup"><span data-stu-id="78a11-127">**ICC\_Auth**</span></span>](iscardauth-icc-auth.md)        | <span data-ttu-id="78a11-128">Consente a un'applicazione di autenticare la smart card.</span><span class="sxs-lookup"><span data-stu-id="78a11-128">Allows an application to authenticate the smart card.</span></span><br/>                               |
| [<span data-ttu-id="78a11-129">**\_Autenticazione utente**</span><span class="sxs-lookup"><span data-stu-id="78a11-129">**User\_Auth**</span></span>](iscardauth-user-auth.md)      | <span data-ttu-id="78a11-130">Consente l'accesso ai servizi di autenticazione utente.</span><span class="sxs-lookup"><span data-stu-id="78a11-130">Allows access to user authentication services.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="78a11-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78a11-131">Requirements</span></span>



| <span data-ttu-id="78a11-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a11-132">Requirement</span></span> | <span data-ttu-id="78a11-133">Valore</span><span class="sxs-lookup"><span data-stu-id="78a11-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78a11-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78a11-134">Minimum supported client</span></span><br/> | <span data-ttu-id="78a11-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="78a11-135">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="78a11-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78a11-136">Minimum supported server</span></span><br/> | <span data-ttu-id="78a11-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78a11-137">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="78a11-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="78a11-138">End of client support</span></span><br/>    | <span data-ttu-id="78a11-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="78a11-139">Windows XP</span></span><br/>                                |
| <span data-ttu-id="78a11-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="78a11-140">End of server support</span></span><br/>    | <span data-ttu-id="78a11-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78a11-141">Windows Server 2003</span></span><br/>                       |



 

 

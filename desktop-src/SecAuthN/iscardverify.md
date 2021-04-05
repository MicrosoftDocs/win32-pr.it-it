---
description: Fornisce servizi per l'impostazione del codice CHV (scheda di verifica del contenitore) e per la verifica dell'utente.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interfaccia ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757016"
---
# <a name="iscardverify-interface"></a><span data-ttu-id="21aa3-103">Interfaccia ISCardVerify</span><span class="sxs-lookup"><span data-stu-id="21aa3-103">ISCardVerify interface</span></span>

<span data-ttu-id="21aa3-104">\[L'interfaccia **ISCardVerify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="21aa3-104">\[The **ISCardVerify** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="21aa3-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21aa3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="21aa3-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="21aa3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="21aa3-107">La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di un [*provider di servizi*](../secgloss/c-gly.md)per [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="21aa3-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="21aa3-108">L'interfaccia **ISCardVerify** fornisce servizi per l'impostazione del codice CHV (scheda di verifica del contenitore) e per la verifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="21aa3-108">The **ISCardVerify** interface provides services for setting CHV (card holder verification) code and for verifying the user.</span></span>

<span data-ttu-id="21aa3-109">La classe **ISCardVerify** è definita per le applicazioni che implementano i criteri CHV specifici dell'applicazione e che hanno una conoscenza approfondita dell'implementazione interna della smart card.</span><span class="sxs-lookup"><span data-stu-id="21aa3-109">The **ISCardVerify** class is defined for applications that implement application-specific CHV policy, and that have a detailed knowledge of the smart card's internal implementation.</span></span>

<span data-ttu-id="21aa3-110">Di seguito è riportato un utilizzo tipico dell'interfaccia **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="21aa3-110">Following is a typical use of the **ISCardVerify** interface.</span></span>

<span data-ttu-id="21aa3-111">La procedura seguente usa **ISCardVerify** per modificare il codice CHV.</span><span class="sxs-lookup"><span data-stu-id="21aa3-111">The following procedure uses **ISCardVerify** to change the CHV code.</span></span>

<span data-ttu-id="21aa3-112">**Per modificare il codice CHV di una smart card**</span><span class="sxs-lookup"><span data-stu-id="21aa3-112">**To change the CHV code of a smart card**</span></span>

1.  <span data-ttu-id="21aa3-113">Creare un'interfaccia **ISCardVerify** (tramite il metodo di interfaccia [**ISCardManage**](iscardmanage.md) corrispondente).</span><span class="sxs-lookup"><span data-stu-id="21aa3-113">Create an **ISCardVerify** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="21aa3-114">Chiamare il metodo [**ChangeCode**](iscardverify-changecode.md) e fornire nuovo codice, specificando se è locale o globale e se è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="21aa3-114">Call the [**ChangeCode**](iscardverify-changecode.md) method and provide new code, specifying if it is local or global and if it is enabled or disabled.</span></span>
3.  <span data-ttu-id="21aa3-115">Rilasciare l'interfaccia **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="21aa3-115">Release the **ISCardVerify** interface.</span></span>

## <a name="members"></a><span data-ttu-id="21aa3-116">Membri</span><span class="sxs-lookup"><span data-stu-id="21aa3-116">Members</span></span>

<span data-ttu-id="21aa3-117">L'interfaccia **ISCardVerify** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="21aa3-117">The **ISCardVerify** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="21aa3-118">**ISCardVerify** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="21aa3-118">**ISCardVerify** also has these types of members:</span></span>

-   [<span data-ttu-id="21aa3-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="21aa3-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21aa3-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="21aa3-120">Methods</span></span>

<span data-ttu-id="21aa3-121">L'interfaccia **ISCardVerify** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="21aa3-121">The **ISCardVerify** interface has these methods.</span></span>



| <span data-ttu-id="21aa3-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="21aa3-122">Method</span></span>                                                        | <span data-ttu-id="21aa3-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21aa3-123">Description</span></span>                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21aa3-124">**ChangeCode**</span><span class="sxs-lookup"><span data-stu-id="21aa3-124">**ChangeCode**</span></span>](iscardverify-changecode.md)                 | <span data-ttu-id="21aa3-125">Modifica il codice CHV corrente.</span><span class="sxs-lookup"><span data-stu-id="21aa3-125">Changes the current CHV code.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="21aa3-126">**ResetSecurityState**</span><span class="sxs-lookup"><span data-stu-id="21aa3-126">**ResetSecurityState**</span></span>](iscardverify-resetsecuritystate.md) | <span data-ttu-id="21aa3-127">Reimposta il [*contesto di sicurezza*](../secgloss/s-gly.md) della smart card.</span><span class="sxs-lookup"><span data-stu-id="21aa3-127">Resets the [*security context*](../secgloss/s-gly.md) of the smart card.</span></span><br/> |
| <span data-ttu-id="21aa3-128">[**Sbloccare**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21aa3-128">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>                       | <span data-ttu-id="21aa3-129">Abilita nuovamente il [*contesto di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="21aa3-129">Re-enables the [*security context*](../secgloss/s-gly.md).</span></span><br/>               |
| [<span data-ttu-id="21aa3-130">**Verificare**</span><span class="sxs-lookup"><span data-stu-id="21aa3-130">**Verify**</span></span>](iscardverify-verify.md)                         | <span data-ttu-id="21aa3-131">Autentica l'utente.</span><span class="sxs-lookup"><span data-stu-id="21aa3-131">Authenticates the user.</span></span><br/>                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="21aa3-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21aa3-132">Requirements</span></span>



| <span data-ttu-id="21aa3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="21aa3-133">Requirement</span></span> | <span data-ttu-id="21aa3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="21aa3-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="21aa3-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21aa3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="21aa3-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="21aa3-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="21aa3-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21aa3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="21aa3-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21aa3-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="21aa3-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="21aa3-139">End of client support</span></span><br/>    | <span data-ttu-id="21aa3-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="21aa3-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="21aa3-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="21aa3-141">End of server support</span></span><br/>    | <span data-ttu-id="21aa3-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21aa3-142">Windows Server 2003</span></span><br/>                       |



 

 

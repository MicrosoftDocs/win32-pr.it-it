---
description: Il programma di installazione imposta il valore della proprietà UserSID sulla rappresentazione di stringa dell'ID di sicurezza (SID) dell'utente che esegue l'installazione. Per altre informazioni, vedere strutture di autorizzazione.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: Proprietà UserSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328551"
---
# <a name="usersid-property"></a><span data-ttu-id="96d58-104">Proprietà UserSID</span><span class="sxs-lookup"><span data-stu-id="96d58-104">UserSID property</span></span>

<span data-ttu-id="96d58-105">Il programma di installazione imposta il valore della proprietà **UserSID** sulla rappresentazione di stringa dell'ID di sicurezza (SID) dell'utente che esegue l'installazione.</span><span class="sxs-lookup"><span data-stu-id="96d58-105">The installer sets the value of the **UserSID** property to the string representation of the security identifier (SID) of the user running the installation.</span></span> <span data-ttu-id="96d58-106">Per altre informazioni, vedere [strutture di autorizzazione](../secauthz/authorization-structures.md).</span><span class="sxs-lookup"><span data-stu-id="96d58-106">For more information, see [Authorization Structures](../secauthz/authorization-structures.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="96d58-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="96d58-107">Default Value</span></span>

<span data-ttu-id="96d58-108">No.</span><span class="sxs-lookup"><span data-stu-id="96d58-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d58-109">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="96d58-109">Remarks</span></span>

<span data-ttu-id="96d58-110">Il Windows Installer impostare questa proprietà in Windows 2000, Windows XP e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="96d58-110">The Windows Installer set this property on Windows 2000, Windows XP and Windows Vista.</span></span> <span data-ttu-id="96d58-111">Questa proprietà non è definita in tutti gli altri sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="96d58-111">This property is not defined on all other operating systems.</span></span>

<span data-ttu-id="96d58-112">Si noti che questa proprietà ha l'attributo speciale che può essere recuperato da un'azione personalizzata posticipata.</span><span class="sxs-lookup"><span data-stu-id="96d58-112">Note that this property has the special attribute that it can be retrieved from a deferred custom action.</span></span> <span data-ttu-id="96d58-113">Un'azione personalizzata eseguita con privilegi elevati può comunque restituire il SID dell'utente nella proprietà **UserSID** .</span><span class="sxs-lookup"><span data-stu-id="96d58-113">A custom action running with elevated privileges can still return the user's SID in **UserSID** property.</span></span> <span data-ttu-id="96d58-114">Per informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="96d58-114">For information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96d58-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96d58-115">Requirements</span></span>



| <span data-ttu-id="96d58-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d58-116">Requirement</span></span> | <span data-ttu-id="96d58-117">Valore</span><span class="sxs-lookup"><span data-stu-id="96d58-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d58-118">Versione</span><span class="sxs-lookup"><span data-stu-id="96d58-118">Version</span></span><br/> | <span data-ttu-id="96d58-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="96d58-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="96d58-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="96d58-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="96d58-121">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96d58-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="96d58-122">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="96d58-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96d58-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96d58-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d58-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96d58-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 

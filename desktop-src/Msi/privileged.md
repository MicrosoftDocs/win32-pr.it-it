---
description: La proprietà Privileged indica se l'installazione viene eseguita nel contesto di privilegi elevati.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Proprietà Privileged
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332844"
---
# <a name="privileged-property"></a><span data-ttu-id="cd93b-103">Proprietà Privileged</span><span class="sxs-lookup"><span data-stu-id="cd93b-103">Privileged property</span></span>

<span data-ttu-id="cd93b-104">La proprietà **Privileged** indica se l'installazione viene eseguita nel contesto di privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="cd93b-104">The **Privileged** property indicates whether the installation is performed in the context of elevated privileges.</span></span> <span data-ttu-id="cd93b-105">Il programma di installazione imposta questa proprietà se l'utente dispone di privilegi di amministratore, se l'applicazione è stata assegnata da un amministratore di sistema o se i criteri utente e computer AlwaysInstallElevated sono impostati su true.</span><span class="sxs-lookup"><span data-stu-id="cd93b-105">The installer sets this property if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="default-value"></a><span data-ttu-id="cd93b-106">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="cd93b-106">Default Value</span></span>

<span data-ttu-id="cd93b-107">Il programma di installazione non imposta questa proprietà se l'utente non è autorizzato a eseguire l'installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="cd93b-107">The installer does not set this property if the user is not allowed to install with elevated privileges.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd93b-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd93b-108">Remarks</span></span>

<span data-ttu-id="cd93b-109">Gli sviluppatori di pacchetti del programma di installazione possono utilizzare la proprietà **Privileged** per rendere l'installazione condizionale sui criteri di sistema, l'utente amministratore o l'assegnazione da parte di un amministratore.</span><span class="sxs-lookup"><span data-stu-id="cd93b-109">Developers of installer packages can use the **Privileged** property to make the installation conditional upon system policy, the user being an administrator, or assignment by an administrator.</span></span>

<span data-ttu-id="cd93b-110">Quando è in esecuzione in Windows Vista, i **privilegi** e [**AdminUser**](adminuser.md) sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="cd93b-110">When running on Windows Vista, the **Privileged** and [**AdminUser**](adminuser.md) are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd93b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd93b-111">Requirements</span></span>



| <span data-ttu-id="cd93b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd93b-112">Requirement</span></span> | <span data-ttu-id="cd93b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cd93b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd93b-114">Versione</span><span class="sxs-lookup"><span data-stu-id="cd93b-114">Version</span></span><br/> | <span data-ttu-id="cd93b-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cd93b-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cd93b-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd93b-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cd93b-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd93b-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cd93b-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cd93b-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd93b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd93b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd93b-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd93b-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 





---
description: Il programma di installazione imposta il valore della proprietà MsiRestartManagerSessionKey sulla chiave di sessione per la sessione di gestione riavvio.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Proprietà MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331081"
---
# <a name="msirestartmanagersessionkey-property"></a><span data-ttu-id="62ef1-103">Proprietà MsiRestartManagerSessionKey</span><span class="sxs-lookup"><span data-stu-id="62ef1-103">MsiRestartManagerSessionKey property</span></span>

<span data-ttu-id="62ef1-104">Il programma di installazione imposta il valore della proprietà **MsiRestartManagerSessionKey** sulla chiave di sessione per la sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="62ef1-104">The installer sets the value of the **MsiRestartManagerSessionKey** property to the session key for the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span> <span data-ttu-id="62ef1-105">Le azioni personalizzate possono utilizzare la chiave della sessione per partecipare alla sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="62ef1-105">Custom actions can use the session key to join the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>

## <a name="remarks"></a><span data-ttu-id="62ef1-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="62ef1-106">Remarks</span></span>

<span data-ttu-id="62ef1-107">Il programma di installazione imposta il valore della proprietà **MsiRestartManagerSessionKey** in fase di inizializzazione, quindi cancella il valore durante l'azione [InstallValidate](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="62ef1-107">The installer sets the value of the **MsiRestartManagerSessionKey** property at initialization, and then clears the value during the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="62ef1-108">Le azioni personalizzate che richiedono il valore della proprietà **MsiRestartManagerSessionKey** devono essere precedenti all'azione InstallValidate nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="62ef1-108">Custom actions that need the value of the **MsiRestartManagerSessionKey** property must be come before the InstallValidate action in the action sequence.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ef1-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62ef1-109">Requirements</span></span>



| <span data-ttu-id="62ef1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ef1-110">Requirement</span></span> | <span data-ttu-id="62ef1-111">Valore</span><span class="sxs-lookup"><span data-stu-id="62ef1-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ef1-112">Versione</span><span class="sxs-lookup"><span data-stu-id="62ef1-112">Version</span></span><br/> | <span data-ttu-id="62ef1-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62ef1-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62ef1-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62ef1-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62ef1-115">Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="62ef1-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62ef1-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62ef1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ef1-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62ef1-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="62ef1-118">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="62ef1-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 

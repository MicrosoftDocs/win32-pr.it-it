---
description: Il programma di installazione imposta la proprietà AFTERREBOOT su 1 dopo un riavvio richiamato dall'azione ForceReboot. Il programma di installazione aggiunge AFTERREBOOT = 1 alla riga di comando eseguita subito dopo il riavvio.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Proprietà AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331620"
---
# <a name="afterreboot-property"></a><span data-ttu-id="6a4e7-104">Proprietà AFTERREBOOT</span><span class="sxs-lookup"><span data-stu-id="6a4e7-104">AFTERREBOOT property</span></span>

<span data-ttu-id="6a4e7-105">Il programma di installazione imposta la proprietà **AFTERREBOOT** su 1 dopo un riavvio richiamato dall' [azione ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a4e7-105">The installer sets the **AFTERREBOOT** property to 1 after a reboot invoked by the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="6a4e7-106">Il programma di installazione aggiunge AFTERREBOOT = 1 alla riga di comando eseguita subito dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-106">The installer adds AFTERREBOOT=1 to the command line run immediately after the reboot.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a4e7-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a4e7-107">Remarks</span></span>

<span data-ttu-id="6a4e7-108">L' [azione ForceReboot](forcereboot-action.md) deve sempre essere utilizzata con un'istruzione condizionale in modo tale che il programma di installazione avvii un riavvio solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-108">The [ForceReboot action](forcereboot-action.md) must always be used with a conditional statement such that the installer triggers a reboot only when necessary.</span></span> <span data-ttu-id="6a4e7-109">Potrebbe essere necessario riavviare il computer se è stato sostituito un particolare file o se è stato installato un particolare componente.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-109">A reboot might be required if a particular file was replaced or a particular component was installed.</span></span> <span data-ttu-id="6a4e7-110">Il caso è diverso per ogni prodotto ed è possibile che sia necessaria un'azione personalizzata per determinare se è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-110">The case is different for each product and a custom action might be needed to determine whether a reboot is needed.</span></span> <span data-ttu-id="6a4e7-111">La condizione sull'azione ForceReboot USA in genere la proprietà **AFTERREBOOT** .</span><span class="sxs-lookup"><span data-stu-id="6a4e7-111">The condition on the ForceReboot action commonly makes use of the **AFTERREBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4e7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a4e7-112">Requirements</span></span>



| <span data-ttu-id="6a4e7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4e7-113">Requirement</span></span> | <span data-ttu-id="6a4e7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6a4e7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4e7-115">Versione</span><span class="sxs-lookup"><span data-stu-id="6a4e7-115">Version</span></span><br/> | <span data-ttu-id="6a4e7-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a4e7-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a4e7-118">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6a4e7-119">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6a4e7-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a4e7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a4e7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4e7-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a4e7-121">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="6a4e7-122">Riavvio del sistema</span><span class="sxs-lookup"><span data-stu-id="6a4e7-122">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 





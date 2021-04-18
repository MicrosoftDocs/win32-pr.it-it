---
description: La proprietà MSIRMSHUTDOWN determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati per consentire l'installazione dell'aggiornamento.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Proprietà MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331079"
---
# <a name="msirmshutdown-property"></a><span data-ttu-id="8a272-103">Proprietà MSIRMSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="8a272-103">MSIRMSHUTDOWN property</span></span>

<span data-ttu-id="8a272-104">La proprietà **MSIRMSHUTDOWN** determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati per consentire l'installazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8a272-104">The **MSIRMSHUTDOWN** property determines how applications or services that are currently using files affected by an update should be shut down to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="8a272-105">Valore</span><span class="sxs-lookup"><span data-stu-id="8a272-105">Value</span></span>



| <span data-ttu-id="8a272-106">Valore</span><span class="sxs-lookup"><span data-stu-id="8a272-106">Value</span></span>                                                                        | <span data-ttu-id="8a272-107">Significato</span><span class="sxs-lookup"><span data-stu-id="8a272-107">Meaning</span></span>                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a272-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8a272-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="8a272-109">I processi o i servizi che attualmente utilizzano i file interessati dall'aggiornamento vengono arrestati.</span><span class="sxs-lookup"><span data-stu-id="8a272-109">Processes or services that are currently using files affected by the update are shut down.</span></span><br/>                                                                                                                                                                   |
| <dl> <span data-ttu-id="8a272-110"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8a272-110"><dt>1</dt></span></span> </dl> | <span data-ttu-id="8a272-111">I processi o i servizi che attualmente utilizzano i file interessati dall'aggiornamento e che non rispondono a [Gestione riavvio](../rstmgr/restart-manager-portal.md)sono costretti ad arrestarsi.</span><span class="sxs-lookup"><span data-stu-id="8a272-111">Processes or services that are currently using files affected by the update, and that do not respond to the [Restart Manager](../rstmgr/restart-manager-portal.md), are forced to shut down.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="8a272-112"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8a272-112"><dt>2</dt></span></span> </dl> | <span data-ttu-id="8a272-113">I processi o i servizi che attualmente utilizzano i file interessati dall'aggiornamento vengono arrestati solo se sono stati registrati per un riavvio.</span><span class="sxs-lookup"><span data-stu-id="8a272-113">Processes or services that are currently using files affected by the update are shut down only if they have all been registered for a restart.</span></span> <span data-ttu-id="8a272-114">Se un processo o un servizio non è stato registrato per il riavvio, non vengono arrestati processi o servizi.</span><span class="sxs-lookup"><span data-stu-id="8a272-114">If any process or service has not been registered for a restart, then no processes or services are shut down.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a272-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a272-115">Remarks</span></span>

<span data-ttu-id="8a272-116">La proprietà **MSIRMSHUTDOWN** viene ignorata se [Gestione riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8a272-116">The **MSIRMSHUTDOWN** property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a272-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a272-117">Requirements</span></span>



| <span data-ttu-id="8a272-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a272-118">Requirement</span></span> | <span data-ttu-id="8a272-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8a272-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a272-120">Versione</span><span class="sxs-lookup"><span data-stu-id="8a272-120">Version</span></span><br/> | <span data-ttu-id="8a272-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8a272-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8a272-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8a272-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8a272-123">Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8a272-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a272-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a272-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a272-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a272-125">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8a272-126">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="8a272-126">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 

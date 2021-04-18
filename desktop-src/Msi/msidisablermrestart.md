---
description: La proprietà MSIDISABLERMRESTART determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati e riavviati per consentire l'installazione dell'aggiornamento.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Proprietà MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329341"
---
# <a name="msidisablermrestart-property"></a><span data-ttu-id="40eca-103">Proprietà MSIDISABLERMRESTART</span><span class="sxs-lookup"><span data-stu-id="40eca-103">MSIDISABLERMRESTART property</span></span>

<span data-ttu-id="40eca-104">La proprietà **MSIDISABLERMRESTART** determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati e riavviati per consentire l'installazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="40eca-104">The **MSIDISABLERMRESTART** property determines how applications or services that are currently using files affected by an update should be shut down and restarted to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="40eca-105">Valore</span><span class="sxs-lookup"><span data-stu-id="40eca-105">Value</span></span>



| <span data-ttu-id="40eca-106">Valore</span><span class="sxs-lookup"><span data-stu-id="40eca-106">Value</span></span>                                                                        | <span data-ttu-id="40eca-107">Significato</span><span class="sxs-lookup"><span data-stu-id="40eca-107">Meaning</span></span>                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40eca-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40eca-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="40eca-109">Tutti i servizi di sistema arrestati per installare l'aggiornamento vengono riavviati.</span><span class="sxs-lookup"><span data-stu-id="40eca-109">All system services that were shut down to install the update are restarted.</span></span> <span data-ttu-id="40eca-110">Tutte le applicazioni registrate con [Gestione riavvio](../rstmgr/restart-manager-portal.md) vengono riavviate.</span><span class="sxs-lookup"><span data-stu-id="40eca-110">All applications that registered themselves with the [Restart Manager](../rstmgr/restart-manager-portal.md) are restarted.</span></span><br/> |
| <dl> <span data-ttu-id="40eca-111"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="40eca-111"><dt>1</dt></span></span> </dl> | <span data-ttu-id="40eca-112">I processi arrestati utilizzando [Gestione riavvio](../rstmgr/restart-manager-portal.md) durante l'installazione dell'aggiornamento non verranno riavviati dopo l'applicazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="40eca-112">Processes that were shut down using the [Restart Manager](../rstmgr/restart-manager-portal.md) while installing the update will not be restarted after the update is applied.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="40eca-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="40eca-113">Remarks</span></span>

<span data-ttu-id="40eca-114">La proprietà **MSIDISABLERMRESTART** viene ignorata se [Gestione riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="40eca-114">The **MSIDISABLERMRESTART** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="40eca-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40eca-115">Requirements</span></span>



| <span data-ttu-id="40eca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="40eca-116">Requirement</span></span> | <span data-ttu-id="40eca-117">Valore</span><span class="sxs-lookup"><span data-stu-id="40eca-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40eca-118">Versione</span><span class="sxs-lookup"><span data-stu-id="40eca-118">Version</span></span><br/> | <span data-ttu-id="40eca-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40eca-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="40eca-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="40eca-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="40eca-121">Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="40eca-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40eca-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40eca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40eca-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="40eca-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="40eca-124">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="40eca-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 

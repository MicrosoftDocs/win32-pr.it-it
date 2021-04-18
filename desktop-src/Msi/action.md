---
description: La proprietà ACTION può essere impostata sui valori seguenti.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Proprietà ACTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329617"
---
# <a name="action-property"></a><span data-ttu-id="e6ebb-103">Proprietà ACTION</span><span class="sxs-lookup"><span data-stu-id="e6ebb-103">ACTION property</span></span>

<span data-ttu-id="e6ebb-104">La proprietà **Action** può essere impostata sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e6ebb-104">The **ACTION** property can be set to the following values.</span></span>

## <a name="value"></a><span data-ttu-id="e6ebb-105">Valore</span><span class="sxs-lookup"><span data-stu-id="e6ebb-105">Value</span></span>



| <span data-ttu-id="e6ebb-106">Valore</span><span class="sxs-lookup"><span data-stu-id="e6ebb-106">Value</span></span>                                                                                                                                            | <span data-ttu-id="e6ebb-107">Significato</span><span class="sxs-lookup"><span data-stu-id="e6ebb-107">Meaning</span></span>                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <span data-ttu-id="e6ebb-108"><dt>**INSTALLARE**</dt></span><span class="sxs-lookup"><span data-stu-id="e6ebb-108"><dt>**INSTALL**</dt></span></span> </dl>       | [<span data-ttu-id="e6ebb-109">Azione di installazione</span><span class="sxs-lookup"><span data-stu-id="e6ebb-109">INSTALL Action</span></span>](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <span data-ttu-id="e6ebb-110"><dt>**PUBBLICIZZARE**</dt></span><span class="sxs-lookup"><span data-stu-id="e6ebb-110"><dt>**ADVERTISE**</dt></span></span> </dl> | [<span data-ttu-id="e6ebb-111">Pubblicizza azione</span><span class="sxs-lookup"><span data-stu-id="e6ebb-111">ADVERTISE Action</span></span>](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <span data-ttu-id="e6ebb-112"><dt>**ADMIN**</dt></span><span class="sxs-lookup"><span data-stu-id="e6ebb-112"><dt>**ADMIN**</dt></span></span> </dl>             | [<span data-ttu-id="e6ebb-113">Azione di amministrazione</span><span class="sxs-lookup"><span data-stu-id="e6ebb-113">ADMIN Action</span></span>](admin-action.md)<br/>         |



 

<span data-ttu-id="e6ebb-114">La proprietà **Action** determina l'azione da eseguire se viene fornito un nome di azione null a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o al [**Metodo DoAction**](session-doaction.md).</span><span class="sxs-lookup"><span data-stu-id="e6ebb-114">The **ACTION** property determines which action to perform if a Null action name is supplied to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) or the [**DoAction Method**](session-doaction.md).</span></span> <span data-ttu-id="e6ebb-115">Se non viene definito alcun valore per la proprietà **Action** , il programma di installazione chiama l' [azione di installazione](install-action.md).</span><span class="sxs-lookup"><span data-stu-id="e6ebb-115">If no value is defined for the **ACTION** property, the installer calls the [INSTALL Action](install-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ebb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6ebb-116">Requirements</span></span>



| <span data-ttu-id="e6ebb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6ebb-117">Requirement</span></span> | <span data-ttu-id="e6ebb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e6ebb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ebb-119">Versione</span><span class="sxs-lookup"><span data-stu-id="e6ebb-119">Version</span></span><br/> | <span data-ttu-id="e6ebb-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6ebb-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6ebb-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6ebb-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6ebb-122">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e6ebb-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e6ebb-123">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e6ebb-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6ebb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6ebb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ebb-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6ebb-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 





---
description: La \_ proprietà dell'unità CCP è impostata sul percorso radice del volume rimovibile che deve essere cercato da RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: Proprietà CCP_DRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327326"
---
# <a name="ccp_drive-property"></a><span data-ttu-id="4ae03-103">\_Proprietà unità CCP</span><span class="sxs-lookup"><span data-stu-id="4ae03-103">CCP\_DRIVE property</span></span>

<span data-ttu-id="4ae03-104">La proprietà dell' **\_ unità CCP** è impostata sul percorso radice del volume rimovibile che deve essere cercato da [RMCCPSearch](rmccpsearch-action.md).</span><span class="sxs-lookup"><span data-stu-id="4ae03-104">The **CCP\_DRIVE** property is set to the root path of the removable volume that is to be searched by [RMCCPSearch](rmccpsearch-action.md).</span></span> <span data-ttu-id="4ae03-105">L'azione RMCCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4ae03-105">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before performing an upgrade installation.</span></span>

<span data-ttu-id="4ae03-106">Questa proprietà viene in genere impostata tramite l'interfaccia utente o un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4ae03-106">This property is typically set via the user interface or a custom action.</span></span> <span data-ttu-id="4ae03-107">Questa proprietà deve essere impostata prima dell'esecuzione dell'azione [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4ae03-107">This property should be set before the [RMCCPSearch](rmccpsearch-action.md) action is run.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae03-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ae03-108">Requirements</span></span>



| <span data-ttu-id="4ae03-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae03-109">Requirement</span></span> | <span data-ttu-id="4ae03-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4ae03-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae03-111">Versione</span><span class="sxs-lookup"><span data-stu-id="4ae03-111">Version</span></span><br/> | <span data-ttu-id="4ae03-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4ae03-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4ae03-113">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ae03-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4ae03-114">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4ae03-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4ae03-115">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4ae03-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ae03-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ae03-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae03-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ae03-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 





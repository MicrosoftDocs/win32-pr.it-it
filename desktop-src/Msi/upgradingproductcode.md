---
description: La proprietà UPGRADINGPRODUCTCODE viene impostata da Windows Installer quando un aggiornamento rimuove un'applicazione.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Proprietà UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328136"
---
# <a name="upgradingproductcode-property"></a><span data-ttu-id="1f7f4-103">Proprietà UPGRADINGPRODUCTCODE</span><span class="sxs-lookup"><span data-stu-id="1f7f4-103">UPGRADINGPRODUCTCODE property</span></span>

<span data-ttu-id="1f7f4-104">La proprietà **UPGRADINGPRODUCTCODE** viene impostata da Windows Installer quando un aggiornamento rimuove un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1f7f4-104">The **UPGRADINGPRODUCTCODE** property is set by Windows Installer when an upgrade removes an application.</span></span> <span data-ttu-id="1f7f4-105">Il programma di installazione imposta questa proprietà quando esegue l' [azione RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="1f7f4-105">The installer sets this property when it runs the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="1f7f4-106">Questa proprietà non viene impostata rimuovendo un'applicazione utilizzando Installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="1f7f4-106">This property is not set by removing an application using the Add or Remove Programs in Control Panel.</span></span> <span data-ttu-id="1f7f4-107">Un'applicazione determina se viene rimossa da un aggiornamento o da installazione applicazioni controllando **UPGRADINGPRODUCTCODE**.</span><span class="sxs-lookup"><span data-stu-id="1f7f4-107">An application determines whether it is being removed by an upgrade or the Add or Remove Programs by checking **UPGRADINGPRODUCTCODE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7f4-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f7f4-108">Requirements</span></span>



| <span data-ttu-id="1f7f4-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f7f4-109">Requirement</span></span> | <span data-ttu-id="1f7f4-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7f4-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7f4-111">Versione</span><span class="sxs-lookup"><span data-stu-id="1f7f4-111">Version</span></span><br/> | <span data-ttu-id="1f7f4-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1f7f4-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1f7f4-113">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1f7f4-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1f7f4-114">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1f7f4-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1f7f4-115">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1f7f4-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f7f4-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f7f4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7f4-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f7f4-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 





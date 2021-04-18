---
description: È possibile utilizzare la proprietà MSIFASTINSTALL per ridurre il tempo necessario per l'installazione di un pacchetto di Windows Installer di grandi dimensioni.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Proprietà MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329122"
---
# <a name="msifastinstall-property"></a><span data-ttu-id="6ebdc-103">Proprietà MSIFASTINSTALL</span><span class="sxs-lookup"><span data-stu-id="6ebdc-103">MSIFASTINSTALL property</span></span>

<span data-ttu-id="6ebdc-104">È possibile utilizzare la proprietà **MSIFASTINSTALL** per ridurre il tempo necessario per l'installazione di un pacchetto di Windows Installer di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-104">The **MSIFASTINSTALL** property can be used to reduce the time required to install a large Windows Installer package.</span></span> <span data-ttu-id="6ebdc-105">La proprietà può essere impostata nella riga di comando o nella tabella delle [Proprietà](property-table.md) per configurare le operazioni che l'utente o lo sviluppatore determina non sono essenziali per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-105">The property can be set on the command line or in the [Property](property-table.md) table to configure operations that the user or developer determines are non-essential for the installation.</span></span>

<span data-ttu-id="6ebdc-106">Il valore della proprietà **MSIFASTINSTALL** può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-106">The value of the **MSIFASTINSTALL** property can be a combination of the following values.</span></span>



| <span data-ttu-id="6ebdc-107">Valore</span><span class="sxs-lookup"><span data-stu-id="6ebdc-107">Value</span></span> | <span data-ttu-id="6ebdc-108">Significato</span><span class="sxs-lookup"><span data-stu-id="6ebdc-108">Meaning</span></span>                                                                      |
|-------|------------------------------------------------------------------------------|
| <span data-ttu-id="6ebdc-109">0</span><span class="sxs-lookup"><span data-stu-id="6ebdc-109">0</span></span>     | <span data-ttu-id="6ebdc-110">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="6ebdc-110">Default value</span></span>                                                                |
| <span data-ttu-id="6ebdc-111">1</span><span class="sxs-lookup"><span data-stu-id="6ebdc-111">1</span></span>     | <span data-ttu-id="6ebdc-112">Nessun punto di ripristino di sistema salvato per questa installazione.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-112">No system restore point is saved for this installation.</span></span>                      |
| <span data-ttu-id="6ebdc-113">2</span><span class="sxs-lookup"><span data-stu-id="6ebdc-113">2</span></span>     | <span data-ttu-id="6ebdc-114">Eseguire solo il [costo del file](file-costing.md) e ignorare il controllo di altri costi.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-114">Perform only [File Costing](file-costing.md) and skip checking other costs.</span></span> |
| <span data-ttu-id="6ebdc-115">4</span><span class="sxs-lookup"><span data-stu-id="6ebdc-115">4</span></span>     | <span data-ttu-id="6ebdc-116">Ridurre la frequenza dei messaggi di stato.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-116">Reduce the frequency of progress messages.</span></span>                                   |



 

<span data-ttu-id="6ebdc-117">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-117">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="6ebdc-118">Questa proprietà è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-118">This property is available beginning with Windows Installer 5.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebdc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ebdc-119">Requirements</span></span>



| <span data-ttu-id="6ebdc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ebdc-120">Requirement</span></span> | <span data-ttu-id="6ebdc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6ebdc-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebdc-122">Versione</span><span class="sxs-lookup"><span data-stu-id="6ebdc-122">Version</span></span><br/> | <span data-ttu-id="6ebdc-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6ebdc-124">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6ebdc-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



 

 





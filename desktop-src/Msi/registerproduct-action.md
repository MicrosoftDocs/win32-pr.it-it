---
description: L'azione RegisterProduct registra le informazioni sul prodotto con il programma di installazione e con installazione applicazioni. Questa azione archivia inoltre il pacchetto di database Windows Installer nel computer locale.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Azione RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311708"
---
# <a name="registerproduct-action"></a><span data-ttu-id="0f00a-104">Azione RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="0f00a-104">RegisterProduct Action</span></span>

<span data-ttu-id="0f00a-105">L'azione RegisterProduct registra le informazioni sul prodotto con il programma di installazione e con installazione applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0f00a-105">The RegisterProduct action registers the product information with the installer and with Add/Remove Programs.</span></span> <span data-ttu-id="0f00a-106">Questa azione archivia inoltre il pacchetto di database Windows Installer nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="0f00a-106">Additionally, this action stores the Windows Installer database package on the local computer.</span></span>

<span data-ttu-id="0f00a-107">L'azione RegisterProduct configura i controlli visualizzati da installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="0f00a-107">The RegisterProduct action configures the controls displayed by the Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="0f00a-108">Per ulteriori informazioni, vedere [configurazione di installazione applicazioni con Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="0f00a-108">For more information, see [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0f00a-109">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="0f00a-109">Sequence Restrictions</span></span>

<span data-ttu-id="0f00a-110">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="0f00a-110">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0f00a-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="0f00a-111">ActionData Messages</span></span>



| <span data-ttu-id="0f00a-112">Campo</span><span class="sxs-lookup"><span data-stu-id="0f00a-112">Field</span></span> | <span data-ttu-id="0f00a-113">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="0f00a-113">Description of action data</span></span>            |
|-------|---------------------------------------|
| <span data-ttu-id="0f00a-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0f00a-114">\[1\]</span></span> | <span data-ttu-id="0f00a-115">Informazioni sul prodotto registrato.</span><span class="sxs-lookup"><span data-stu-id="0f00a-115">Information about registered product.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0f00a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f00a-116">Remarks</span></span>

<span data-ttu-id="0f00a-117">L'azione RegisterProduct non viene eseguita durante l'installazione in un punto di installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="0f00a-117">The RegisterProduct action is not performed during installation to an administrative installation point.</span></span>

 

 




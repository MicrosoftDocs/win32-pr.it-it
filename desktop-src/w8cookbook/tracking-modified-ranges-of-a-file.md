---
title: Rilevamento degli intervalli modificati di un file
description: Rilevamento degli intervalli modificati di un file
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300565"
---
# <a name="tracking-modified-ranges-of-a-file"></a><span data-ttu-id="0cfe5-103">Rilevamento degli intervalli modificati di un file</span><span class="sxs-lookup"><span data-stu-id="0cfe5-103">Tracking modified ranges of a file</span></span>

## <a name="platforms"></a><span data-ttu-id="0cfe5-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="0cfe5-104">Platforms</span></span>

<span data-ttu-id="0cfe5-105">**Client-** Windows 8.1 (tutti gli SKU)</span><span class="sxs-lookup"><span data-stu-id="0cfe5-105">**Clients -** Windows 8.1 (all SKUs)</span></span>  
<span data-ttu-id="0cfe5-106">**Server-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0cfe5-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="0cfe5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cfe5-107">Description</span></span>

<span data-ttu-id="0cfe5-108">Il team NT file System (NTFS) ha aggiunto una nuova funzionalità di Windows.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-108">The NT File System (NTFS) team has added a new feature to Windows.</span></span> <span data-ttu-id="0cfe5-109">Il journal USN restituirà un record di numero di sequenza di aggiornamento (USN) contenente intervalli modificati per un file alla chiusura.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-109">USN Journal will output an update sequence number (USN) record containing modified ranges for a file upon close.</span></span> <span data-ttu-id="0cfe5-110">È stato introdotto un nuovo tipo \_ di record, record USN \_ V4 per registrare gli intervalli modificati di un file.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-110">A new record type, USN\_RECORD\_V4 has been introduced to record these changed ranges of a file.</span></span>

<span data-ttu-id="0cfe5-111">La funzionalità non è abilitata per impostazione predefinita. Gli utenti devono richiamare un comando di controllo file system (FSCTL) per abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-111">The feature is not enabled by default; users must invoke a file system control (FSCTL) command to enable it.</span></span> <span data-ttu-id="0cfe5-112">Tuttavia, poiché altri componenti di Windows possono attivare il rilevamento dell'intervallo, gli utenti e gli sviluppatori possono percepire che la funzionalità è sempre abilitata.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-112">However, because other Windows components may turn on range tracking, users and developers may perceive that the feature is always enabled.</span></span> <span data-ttu-id="0cfe5-113">Windows consentirà agli sviluppatori di eseguire query sul journal USN per verificare se il rilevamento dell'intervallo è abilitato.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-113">Windows will allow developers to query USN journal to find out if range tracking is enabled.</span></span>

<span data-ttu-id="0cfe5-114">La documentazione MSDN verrà fornita in un secondo momento per indicare agli sviluppatori come accedere ai \_ record USN record \_ V4.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-114">MSDN documentation will be provided at a later date to instruct developers in how to access USN\_RECORD\_V4 records.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0cfe5-115">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="0cfe5-115">Manifestation</span></span>

<span data-ttu-id="0cfe5-116">Tutte le applicazioni esistenti che utilizzano il journal USN continueranno a funzionare correttamente senza problemi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-116">All existing applications that use USN Journal will continue to work well without any compatibility issues.</span></span>

 

 





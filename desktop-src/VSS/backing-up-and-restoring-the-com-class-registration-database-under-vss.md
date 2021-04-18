---
description: Il Component Object Model (COM) è uno standard binario per la scrittura di software componente in un ambiente di elaborazione distribuito.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Backup e ripristino del database di registrazione della classe COM+ in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318913"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a><span data-ttu-id="6a255-103">Backup e ripristino del database di registrazione della classe COM+ in VSS</span><span class="sxs-lookup"><span data-stu-id="6a255-103">Backing Up and Restoring the COM+ Class Registration Database Under VSS</span></span>

<span data-ttu-id="6a255-104">Il Component Object Model (COM) è uno standard binario per la scrittura di software componente in un ambiente di elaborazione distribuito.</span><span class="sxs-lookup"><span data-stu-id="6a255-104">The Component Object Model (COM) is a binary standard for writing component software in a distributed computing environment.</span></span>

<span data-ttu-id="6a255-105">Gli identificatori dei componenti archiviati (GUID) dell'implementazione Win32 originale e altri Stati COM nel registro di sistema in **HKEY \_ classi \_ radice \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="6a255-105">The original Win32 implementation stored component identifiers (GUIDs) and other COM state in the registry under **HKEY\_CLASSES\_ROOT\\CLSID**.</span></span>

<span data-ttu-id="6a255-106">La generazione corrente del Component Object Model, COM+, offre un database indipendente dal registro di sistema per l'archiviazione delle informazioni di registrazione dei componenti, ovvero il database di registrazione della classe COM+.</span><span class="sxs-lookup"><span data-stu-id="6a255-106">The current generation of the Component Object Model, COM+, offers a registry-independent database for storing component registration information: the COM+ Class Registration Database.</span></span>

<span data-ttu-id="6a255-107">Il database di registrazione della classe COM+ supporta una VSS writer, che consente ai richiedenti di eseguire il backup del database di registrazione usando i dati archiviati in un volume copiato in Shadow.</span><span class="sxs-lookup"><span data-stu-id="6a255-107">The COM+ Class Registration Database supports a VSS writer, which allows requesters to back up the registration database using data stored on a shadow-copied volume.</span></span>

<span data-ttu-id="6a255-108">Per ripristinare il database di registrazione COM+, un richiedente deve chiamare il metodo [ICOMAdminCatalog:: RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="6a255-108">To restore the COM+ Registration Database, a requester must call the [ICOMAdminCatalog::RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="6a255-109">Per ulteriori informazioni sul writer del database di registrazione COM+, vedere la pagina relativa ai [writer VSS](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="6a255-109">For more information about the COM+ Registration Database writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 

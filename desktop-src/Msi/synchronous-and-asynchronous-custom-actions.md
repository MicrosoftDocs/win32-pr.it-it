---
description: Il Windows Installer elabora le azioni personalizzate come thread separato dall'installazione principale.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Azioni personalizzate sincrone e asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308675"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a><span data-ttu-id="4f1ec-103">Azioni personalizzate sincrone e asincrone</span><span class="sxs-lookup"><span data-stu-id="4f1ec-103">Synchronous and Asynchronous Custom Actions</span></span>

<span data-ttu-id="4f1ec-104">Il Windows Installer elabora le azioni personalizzate come thread separato dall'installazione principale.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-104">The Windows Installer processes custom actions as a separate thread from the main installation.</span></span> <span data-ttu-id="4f1ec-105">Durante l'esecuzione sincrona di un'azione personalizzata, il programma di installazione attende il completamento del thread dell'azione personalizzata prima di continuare l'installazione principale.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-105">During synchronous execution of a custom action, the installer waits for the thread of the custom action to complete before continuing the main installation.</span></span> <span data-ttu-id="4f1ec-106">Durante l'esecuzione asincrona, il programma di installazione esegue l'azione personalizzata contemporaneamente mentre l'installazione corrente continua.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-106">During asynchronous execution, the installer runs the custom action simultaneously as the current installation continues.</span></span> <span data-ttu-id="4f1ec-107">Gli autori di azioni personalizzate devono pertanto essere a conoscenza di eventuali thread asincroni che possono apportare modifiche al database di installazione tra le chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-107">Authors of custom actions must therefore be aware of any asynchronous threads that may be making changes to the installation database between function calls.</span></span>

<span data-ttu-id="4f1ec-108">In particolare, le chiamate a [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) e [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) devono essere evitate in azioni personalizzate asincrone.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-108">In particular, calls to [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) and [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) should be avoided in asynchronous custom actions.</span></span> <span data-ttu-id="4f1ec-109">Usare invece [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) per ottenere un percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-109">Instead use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) to obtain a target path.</span></span> <span data-ttu-id="4f1ec-110">Le operazioni di database bulk, ad esempio le operazioni di importazione, esportazione e trasformazione, devono essere evitate in qualsiasi tipo di azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-110">Bulk database operations such as import, export, and transform operations should be avoided in any type of custom action.</span></span>

<span data-ttu-id="4f1ec-111">I flag di opzione possono essere impostati nel campo Type della [tabella CustomAction](customaction-table.md) per specificare che i thread delle azioni principale e personalizzata vengono eseguiti in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-111">Option flags can be set in the Type field of the [CustomAction table](customaction-table.md) to specify that the main and custom action threads run synchronously or asynchronously.</span></span> <span data-ttu-id="4f1ec-112">Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="4f1ec-112">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="4f1ec-113">Il programma di installazione può eseguire azioni [personalizzate di rollback](rollback-custom-actions.md) e azioni di [installazione simultanee](concurrent-installations.md) come azioni personalizzate sincrone.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-113">The installer can only execute [Rollback Custom Actions](rollback-custom-actions.md) and [Concurrent Installation](concurrent-installations.md) actions as synchronous custom actions.</span></span>

 

 




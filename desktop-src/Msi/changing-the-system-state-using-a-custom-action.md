---
description: Le azioni personalizzate progettate per modificare lo stato del sistema devono essere azioni personalizzate di esecuzione posticipata.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Modifica dello stato del sistema mediante un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310993"
---
# <a name="changing-the-system-state-using-a-custom-action"></a><span data-ttu-id="086f7-103">Modifica dello stato del sistema mediante un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="086f7-103">Changing the System State Using a Custom Action</span></span>

<span data-ttu-id="086f7-104">Le azioni personalizzate progettate per modificare lo stato del sistema devono essere azioni personalizzate di esecuzione posticipata.</span><span class="sxs-lookup"><span data-stu-id="086f7-104">Custom actions intended to change the system state must be deferred execution custom actions.</span></span> <span data-ttu-id="086f7-105">Le azioni personalizzate che impostano le proprietà, gli Stati delle funzionalità, gli Stati dei componenti o le directory di destinazione o pianificano le operazioni di sistema inserendo righe nelle tabelle di sequenza possono utilizzare l'esecuzione immediata in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="086f7-105">Custom actions that set properties, feature states, component states, or target directories, or schedule system operations by inserting rows into sequence tables can use immediate execution safely.</span></span> <span data-ttu-id="086f7-106">Tuttavia, le azioni personalizzate che modificano direttamente il sistema o chiamano un altro servizio di sistema devono essere rinviate al momento in cui viene eseguito lo script di installazione.</span><span class="sxs-lookup"><span data-stu-id="086f7-106">However, custom actions that change the system directly or call another system service must be deferred to the time when the installation script is executed.</span></span> <span data-ttu-id="086f7-107">Per altre informazioni, vedere [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="086f7-107">For more information, see [Deferred Execution Custom Actions](deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="086f7-108">Non tentare di utilizzare un'azione personalizzata di esecuzione immediata per modificare lo stato del sistema, poiché ogni azione personalizzata che modifica lo stato deve disporre di un'azione di rollback personalizzata corrispondente per annullare la modifica dello stato del sistema in caso di rollback dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="086f7-108">You should not attempt to use an immediate execution custom action to change the system state, because every custom action that changes the state needs to have a corresponding rollback custom action to undo the system state change on an installation rollback.</span></span> <span data-ttu-id="086f7-109">Tutte le azioni personalizzate di rollback sono anche azioni personalizzate posticipate e devono precedere l'azione che vengono annullate.</span><span class="sxs-lookup"><span data-stu-id="086f7-109">All rollback custom actions are also deferred custom actions and must precede the action they undo.</span></span> <span data-ttu-id="086f7-110">Per altre informazioni, vedere [rollback delle azioni personalizzate](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="086f7-110">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 




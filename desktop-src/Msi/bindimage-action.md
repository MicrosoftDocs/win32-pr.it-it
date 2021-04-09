---
description: L'azione azione BindImage sul associa ogni file eseguibile o DLL che deve essere associato alle DLL importate da tale file.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Azione azione BindImage sul
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881082"
---
# <a name="bindimage-action"></a><span data-ttu-id="0c8eb-103">Azione azione BindImage sul</span><span class="sxs-lookup"><span data-stu-id="0c8eb-103">BindImage Action</span></span>

<span data-ttu-id="0c8eb-104">L'azione azione BindImage sul associa ogni file eseguibile o DLL che deve essere associato alle DLL importate da tale file.</span><span class="sxs-lookup"><span data-stu-id="0c8eb-104">The BindImage action binds each executable or DLL that must be bound to the DLLs imported by it.</span></span> <span data-ttu-id="0c8eb-105">L'azione azione BindImage sul agisce su ogni file nella tabella [azione BindImage sul](bindimage-table.md) , ma solo su quelli che devono essere installati localmente.</span><span class="sxs-lookup"><span data-stu-id="0c8eb-105">The BindImage action acts on each file in the [BindImage](bindimage-table.md) table, but only those that are to be installed locally.</span></span> <span data-ttu-id="0c8eb-106">Il programma di installazione calcola l'indirizzo virtuale di ogni funzione importata da tutte le dll, quindi Salva l'indirizzo virtuale calcolato nella [*tabella degli indirizzi di importazione*](i-gly.md) (IAT) dell'immagine di importazione.</span><span class="sxs-lookup"><span data-stu-id="0c8eb-106">The installer computes the virtual address of each function imported from all DLLs, then saves the computed virtual address in the importing image's [*import address table*](i-gly.md) (IAT).</span></span>

<span data-ttu-id="0c8eb-107">L'azione azione BindImage sul chiama internamente l'API Windows **BindImageEx** .</span><span class="sxs-lookup"><span data-stu-id="0c8eb-107">The BindImage Action internally calls the **BindImageEx** Windows API.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0c8eb-108">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="0c8eb-108">Sequence Restrictions</span></span>

<span data-ttu-id="0c8eb-109">L'azione azione BindImage sul deve essere successiva all'azione [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0c8eb-109">The BindImage action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0c8eb-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="0c8eb-110">ActionData Messages</span></span>



| <span data-ttu-id="0c8eb-111">Campo</span><span class="sxs-lookup"><span data-stu-id="0c8eb-111">Field</span></span> | <span data-ttu-id="0c8eb-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="0c8eb-112">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="0c8eb-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0c8eb-113">\[1\]</span></span> | <span data-ttu-id="0c8eb-114">Identificatore di file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="0c8eb-114">File identifier of executable.</span></span> |



 

 

 




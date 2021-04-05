---
description: Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 bit o 64 bit.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Azioni personalizzate a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756260"
---
# <a name="64-bit-custom-actions"></a><span data-ttu-id="d9b51-103">Azioni personalizzate a 64 bit</span><span class="sxs-lookup"><span data-stu-id="d9b51-103">64-Bit Custom Actions</span></span>

<span data-ttu-id="d9b51-104">Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="d9b51-104">On 64-bit operating systems, Windows Installer may call custom actions that have been compiled for 32-bit or 64-bit systems.</span></span>

<span data-ttu-id="d9b51-105">Un'azione personalizzata a 64 bit basata sugli [script](scripts.md) deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico azioni personalizzate nella colonna Type della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9b51-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction table](customaction-table.md).</span></span>



| <span data-ttu-id="d9b51-106">Costante</span><span class="sxs-lookup"><span data-stu-id="d9b51-106">Constant</span></span>                             | <span data-ttu-id="d9b51-107">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="d9b51-107">Hexadecimal</span></span> | <span data-ttu-id="d9b51-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="d9b51-108">Decimal</span></span> | <span data-ttu-id="d9b51-109">Significato</span><span class="sxs-lookup"><span data-stu-id="d9b51-109">Meaning</span></span>                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| <span data-ttu-id="d9b51-110">**msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="d9b51-110">**msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="d9b51-111">0x0001000</span><span class="sxs-lookup"><span data-stu-id="d9b51-111">0x0001000</span></span>   | <span data-ttu-id="d9b51-112">4096</span><span class="sxs-lookup"><span data-stu-id="d9b51-112">4096</span></span>    | <span data-ttu-id="d9b51-113">Si tratta di un'azione personalizzata a 64 bit scritta negli [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="d9b51-113">This is a 64-bit custom action written in [Scripts](scripts.md).</span></span> |



 

<span data-ttu-id="d9b51-114">Le azioni personalizzate basate su [file eseguibili](executable-files.md) o [librerie a collegamento dinamico](dynamic-link-libraries.md) che sono state soddisfatte per i sistemi operativi a 64 bit non richiedono l'inclusione di questo bit aggiuntivo nella colonna Type della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="d9b51-114">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that have been complied for a 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction table.</span></span>

 

 




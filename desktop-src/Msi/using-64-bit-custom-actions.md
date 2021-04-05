---
description: Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 o 64 bit.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Uso di azioni personalizzate a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967899"
---
# <a name="using-64-bit-custom-actions"></a><span data-ttu-id="41743-103">Uso di azioni personalizzate a 64 bit</span><span class="sxs-lookup"><span data-stu-id="41743-103">Using 64-bit Custom Actions</span></span>

<span data-ttu-id="41743-104">Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="41743-104">On 64-bit operating systems, Windows Installer can call custom actions that are compiled for 32-bit or 64-bit systems.</span></span> <span data-ttu-id="41743-105">Un'azione personalizzata a 64 bit basata sugli [script](scripts.md) deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico dell'azione personalizzata nella colonna Type della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="41743-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom action numeric type in the Type column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="41743-106">Le azioni personalizzate basate su [file eseguibili](executable-files.md) o [librerie a collegamento dinamico](dynamic-link-libraries.md) conformi ai sistemi operativi a 64 bit non richiedono l'inclusione di questo bit aggiuntivo nella colonna Type della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="41743-106">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that are complied for 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction Table.</span></span>

<span data-ttu-id="41743-107">Per altre informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="41743-107">For more information, see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

 

 




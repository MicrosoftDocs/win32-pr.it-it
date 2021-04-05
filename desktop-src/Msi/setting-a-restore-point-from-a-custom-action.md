---
description: Le azioni personalizzate non devono chiamare la funzione SRSetRestorePoint perché questo può comportare la scrittura di un punto di ingresso di ripristino nel mezzo di un'installazione di Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Impostazione di un punto di ripristino da un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131942"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a><span data-ttu-id="e5097-103">Impostazione di un punto di ripristino da un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="e5097-103">Setting a Restore Point from a Custom Action</span></span>

<span data-ttu-id="e5097-104">Le azioni personalizzate non devono chiamare la funzione [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) perché questo può comportare la scrittura di un punto di ingresso di ripristino nel mezzo di un'installazione di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e5097-104">Custom actions must not call the [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) function because this may result in a restore entry point being written into the middle of a Windows Installer installation.</span></span>

<span data-ttu-id="e5097-105">Per ulteriori informazioni, vedere [punti di ripristino del sistema e il Windows Installer](system-restore-points-and-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="e5097-105">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md).</span></span>

 

 

---
description: Si tratta di un criterio di sistema per computer che può essere utilizzato quando l'amministratore desidera che siano installate solo le applicazioni per computer.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128391"
---
# <a name="disableuserinstalls"></a><span data-ttu-id="26c0a-103">DisableUserInstalls</span><span class="sxs-lookup"><span data-stu-id="26c0a-103">DisableUserInstalls</span></span>

<span data-ttu-id="26c0a-104">Si tratta di un criterio di [sistema](system-policy.md) per computer che può essere utilizzato quando l'amministratore desidera che siano installate solo le applicazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="26c0a-104">This is a per-machine [system policy](system-policy.md) that can be used when the administrator only wants per-machine applications installed.</span></span>

<span data-ttu-id="26c0a-105">Se questo criterio non è impostato, il programma di installazione cerca le applicazioni nel registro di sistema nell'ordine seguente: applicazioni gestite registrate come per utente, applicazioni non gestite registrate come per utente e infine applicazioni registrate come per computer.</span><span class="sxs-lookup"><span data-stu-id="26c0a-105">If this policy is not set, the installer searches the registry for applications in the following order: managed applications registered as per-user, unmanaged applications registered as per-user, and finally applications registered as per-machine.</span></span>

<span data-ttu-id="26c0a-106">Se questo criterio è impostato su 1, il programma di installazione ignorerà tutte le applicazioni registrate come per singolo utente e cercherà solo le applicazioni registrate come per computer.</span><span class="sxs-lookup"><span data-stu-id="26c0a-106">If this policy is set to 1, the installer ignores all applications registered as per-user and only searches for applications registered as per-machine.</span></span> <span data-ttu-id="26c0a-107">Le chiamate al Windows Installer Application Programming Interface o al sistema ignorano le applicazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="26c0a-107">Calls to the Windows Installer application programming interface or system ignore per-user applications.</span></span> <span data-ttu-id="26c0a-108">Il tentativo di eseguire un'installazione nel [contesto di installazione](installation-context.md) per utente fa in modo che il programma di installazione visualizzi un messaggio di errore e interrompa l'installazione.</span><span class="sxs-lookup"><span data-stu-id="26c0a-108">An attempt to perform an installation in the per-user [installation context](installation-context.md) causes the installer to display an error message and stops the installation.</span></span> <span data-ttu-id="26c0a-109">In questo caso, il Windows Installer impedisce inoltre le installazioni per utente da un server terminal.</span><span class="sxs-lookup"><span data-stu-id="26c0a-109">In this case, the Windows Installer also prevents per-user installations from a terminal server.</span></span>

## <a name="registry-key"></a><span data-ttu-id="26c0a-110">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="26c0a-110">Registry Key</span></span>

<span data-ttu-id="26c0a-111">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="26c0a-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="26c0a-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="26c0a-112">Data Type</span></span>

<span data-ttu-id="26c0a-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="26c0a-113">**REG\_DWORD**</span></span>

 

 




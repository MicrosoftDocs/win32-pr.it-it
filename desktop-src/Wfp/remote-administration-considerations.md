---
description: Esistono alcune considerazioni specifiche per i sistemi amministrati in remoto.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considerazioni sull'amministrazione remota di WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316018"
---
# <a name="wfp-remote-administration-considerations"></a><span data-ttu-id="f4c5b-103">Considerazioni sull'amministrazione remota di WFP</span><span class="sxs-lookup"><span data-stu-id="f4c5b-103">WFP Remote Administration Considerations</span></span>

<span data-ttu-id="f4c5b-104">Esistono alcune considerazioni specifiche per i sistemi amministrati in remoto.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-104">There are some considerations that are unique to remotely administered systems.</span></span> <span data-ttu-id="f4c5b-105">In primo luogo, quando l'installazione del software viene distribuita in modalità remota (tramite SMS o MSI), le finestre di dialogo di errore di WFP vengono visualizzate sullo schermo di un amministratore connesso localmente (se presente) e non del servizio di installazione.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-105">First, when software installation is remotely deployed (using SMS or MSI), WFP error dialog boxes are displayed on the screen of a locally logged on administrator (if present), not to the installation service.</span></span> <span data-ttu-id="f4c5b-106">In secondo luogo, se un amministratore accede a un server terminal in remoto e installa un'applicazione che sostituisce i file di sistema protetti, le finestre di dialogo di errore WFP vengono visualizzate solo nella console principale, non nella finestra remota dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-106">Second, if an administrator logs into a terminal server remotely and installs an application that replaces protected system files, the WFP error dialog boxes are displayed only in the main console, not the administrator's remote window.</span></span>

<span data-ttu-id="f4c5b-107">Per questi motivi, Pam disattiva le finestre di dialogo di errore fino a quando un amministratore non esegue l'accesso in locale.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-107">For these reasons, WFP suppresses its error dialog boxes until an administrator logs on locally.</span></span> <span data-ttu-id="f4c5b-108">Gli amministratori remoti possono trovare errori di sostituzione del file nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-108">Remote administrators can find file replacement errors in the system event log.</span></span>

<span data-ttu-id="f4c5b-109">**Windows Vista e Windows Server 2008:** Amministrazione remota WFP non supportata.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-109">**Windows Vista and Windows Server 2008:** WFP remote administration is not supported.</span></span>

 

 




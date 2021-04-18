---
description: Il servizio Windows Installer utilizza la lingua dell'utente corrente in tutte le finestre di dialogo fino a quando non viene aperto un pacchetto di Windows Installer.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localizzazione della lingua visualizzata dalle finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314205"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a><span data-ttu-id="bb82d-103">Localizzazione della lingua visualizzata dalle finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="bb82d-103">Localizing the Language Displayed by Dialogs</span></span>

<span data-ttu-id="bb82d-104">Il servizio Windows Installer utilizza la lingua dell'utente corrente in tutte le finestre di dialogo fino a quando non viene aperto un pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bb82d-104">The Windows Installer service uses the current user's language in all dialogs until a Windows Installer package is opened.</span></span> <span data-ttu-id="bb82d-105">Il Windows Installer determina l'uso di **GetUserDefaultUILanguage**.</span><span class="sxs-lookup"><span data-stu-id="bb82d-105">The Windows Installer determines this by using **GetUserDefaultUILanguage**.</span></span> <span data-ttu-id="bb82d-106">Quando viene aperto un pacchetto di Windows Installer, il programma di installazione Visualizza i dialoghi usando la lingua del pacchetto, come specificato dalla proprietà di [**Riepilogo del modello**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="bb82d-106">When a Windows Installer package is opened, the installer displays dialogs using the package's language as specified by the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="bb82d-107">Per ulteriori informazioni sulla localizzazione della lingua di un pacchetto di Windows Installer, vedere anche [un esempio di localizzazione](a-localization-example.md).</span><span class="sxs-lookup"><span data-stu-id="bb82d-107">For more information about localizing the language of a Windows Installer package, see also [A Localization Example](a-localization-example.md).</span></span>

 

 




---
description: Se il criterio di sistema per computer è impostato su &\# 0034; 1&\# 0034;, il programma di installazione non richiede agli utenti quando gli script all'interno di una pagina Web utilizzano l'interfaccia di automazione del programma di installazione.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309448"
---
# <a name="safeforscripting"></a><span data-ttu-id="a6635-103">SafeForScripting</span><span class="sxs-lookup"><span data-stu-id="a6635-103">SafeForScripting</span></span>

<span data-ttu-id="a6635-104">Se il [criterio di sistema](system-policy.md) per computer è impostato su "1", il programma di installazione non richiede agli utenti quando gli script all'interno di una pagina Web utilizzano l' [interfaccia di automazione](automation-interface.md)del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="a6635-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer does not prompt users when scripts within a Web page use the installer's [automation interface](automation-interface.md).</span></span>

<span data-ttu-id="a6635-105">Prima di impostare questo criterio, è necessario valutare se la richiesta di conferma da parte dell'utente fornisca un livello di sicurezza appropriato per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="a6635-105">Before setting this policy, you should consider whether foregoing the user prompt provides an appropriate level of security for your users.</span></span> <span data-ttu-id="a6635-106">Se questo criterio non è impostato, quando uno script ospitato da un browser Internet tenta di installare un'applicazione, il sistema avvisa l'utente e chiede di accettare o rifiutare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a6635-106">If this policy is not set, when a script hosted by an Internet browser tries to install an application, the system warns the user and asks them to accept or refuse the installation.</span></span> <span data-ttu-id="a6635-107">L'impostazione di SafeForScripting evita questo avviso e può consentire l'installazione di applicazioni nel sistema senza la conoscenza dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a6635-107">Setting SafeForScripting suppresses this warning and may allow the installation of applications on the system without the user's knowledge.</span></span> <span data-ttu-id="a6635-108">Questo criterio può essere utile per un'azienda che usa strumenti basati sul Web per distribuire i programmi.</span><span class="sxs-lookup"><span data-stu-id="a6635-108">This policy may be useful for an enterprise that uses web-based tools to distribute programs.</span></span>

<span data-ttu-id="a6635-109">Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md) e [il download di un'installazione da Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="a6635-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="a6635-110">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a6635-110">Registry Key</span></span>

<span data-ttu-id="a6635-111">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="a6635-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a6635-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a6635-112">Data Type</span></span>

<span data-ttu-id="a6635-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6635-113">**REG\_DWORD**</span></span>

 

 




---
description: Microsoft Windows Installer accetta una Uniform Resource Locator (URL) come origine valida per una patch.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Download e installazione di una patch da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129975"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a><span data-ttu-id="e05a7-103">Download e installazione di una patch da Internet</span><span class="sxs-lookup"><span data-stu-id="e05a7-103">Downloading and Installing a Patch From the Internet</span></span>

<span data-ttu-id="e05a7-104">Microsoft Windows Installer accetta una Uniform Resource Locator (URL) come origine valida per una [patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="e05a7-104">Microsoft Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for a [patch](patch-packages.md).</span></span> <span data-ttu-id="e05a7-105">Per installare una patch che si trova in un server Web in https://MyWeb/MyPatch.msp , utilizzare la riga di comando seguente:</span><span class="sxs-lookup"><span data-stu-id="e05a7-105">To install a patch located on a web server at https://MyWeb/MyPatch.msp, use the following command line:</span></span>

<span data-ttu-id="e05a7-106">**msiexec/p https://MyWeb/MyPatch.msp**</span><span class="sxs-lookup"><span data-stu-id="e05a7-106">**msiexec /p https://MyWeb/MyPatch.msp**</span></span>

<span data-ttu-id="e05a7-107">Per evitare risultati imprevisti, non avviare una patch facendo clic sul collegamento nella pagina Web che mostra l'URL del file di patch.</span><span class="sxs-lookup"><span data-stu-id="e05a7-107">To avoid unexpected results, do not launch a patch by clicking the link on the webpage showing the patch file's URL.</span></span> <span data-ttu-id="e05a7-108">È anche possibile installare una patch usando uno script simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="e05a7-108">You can also install a patch by using a script like the following:</span></span>


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="e05a7-109">Si noti che poiché l'oggetto del [**programma di installazione**](installer-object.md) non è contrassegnato come [SafeForScripting](safeforscripting.md) nel computer dell'utente, gli utenti devono modificare le impostazioni di sicurezza del browser affinché l'esempio funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="e05a7-109">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="e05a7-110">Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="e05a7-110">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e05a7-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e05a7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e05a7-112">Pacchetti patch</span><span class="sxs-lookup"><span data-stu-id="e05a7-112">Patch Packages</span></span>](patch-packages.md)
</dt> <dt>

[<span data-ttu-id="e05a7-113">Creazione di un pacchetto di patch</span><span class="sxs-lookup"><span data-stu-id="e05a7-113">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="e05a7-114">Applicazione di patch a applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="e05a7-114">Patching Customized Applications</span></span>](patching-customized-applications.md)
</dt> <dt>

[<span data-ttu-id="e05a7-115">Download di un'installazione da Internet</span><span class="sxs-lookup"><span data-stu-id="e05a7-115">Downloading an Installation From the Internet</span></span>](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 




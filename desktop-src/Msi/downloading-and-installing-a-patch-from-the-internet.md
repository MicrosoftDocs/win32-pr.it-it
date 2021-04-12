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
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Download e installazione di una patch da Internet

Microsoft Windows Installer accetta una Uniform Resource Locator (URL) come origine valida per una [patch](patch-packages.md). Per installare una patch che si trova in un server Web in https://MyWeb/MyPatch.msp , utilizzare la riga di comando seguente:

**msiexec/p https://MyWeb/MyPatch.msp**

Per evitare risultati imprevisti, non avviare una patch facendo clic sul collegamento nella pagina Web che mostra l'URL del file di patch. È anche possibile installare una patch usando uno script simile al seguente:


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



Si noti che poiché l'oggetto del [**programma di installazione**](installer-object.md) non è contrassegnato come [SafeForScripting](safeforscripting.md) nel computer dell'utente, gli utenti devono modificare le impostazioni di sicurezza del browser affinché l'esempio funzioni correttamente.

Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pacchetti patch](patch-packages.md)
</dt> <dt>

[Creazione di un pacchetto di patch](creating-a-patch-package.md)
</dt> <dt>

[Applicazione di patch a applicazioni personalizzate](patching-customized-applications.md)
</dt> <dt>

[Download di un'installazione da Internet](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 




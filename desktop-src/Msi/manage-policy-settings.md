---
description: Il file VBScript WiPolicy.vbs disponibile in Windows SDK Components for Windows Installer Developers. Questo esempio illustra come usare lo script per gestire i criteri di sistema. I criteri possono essere configurati da un amministratore usando Criteri di gruppo Editor criteri di gruppo.
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Gestione delle impostazioni dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1261c48ec7cc7e51a8556b7565075fa9e92bd60481da08f4f311a3de995a91f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945607"
---
# <a name="manage-policy-settings"></a>Gestione delle impostazioni dei criteri

Il file VBScript WiPolicy.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per gestire i [criteri di sistema](system-policy.md). I criteri possono essere configurati da un amministratore usando Criteri di gruppo Editor criteri di gruppo.

Questo esempio illustra i criteri Windows Installer.

L'uso di questo esempio richiede CScript.exe o WScript.exe versione di Windows Script Host. Per usare CScript.exe eseguire questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con vbs > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script non riesce.

**Valore dei criteri WiPolicy.vbs \[ \] \[ cscript\]**

Se non viene specificato alcun argomento nella riga di comando, l'esempio restituisce le impostazioni dei criteri correnti. Specificare i criteri da impostare usando i codici identificatore seguenti. Specificare il nuovo valore per il criterio. Per restituire il valore corrente di un criterio, specificare una stringa vuota "" per il valore.



| CODE | Descrizione                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Modalità di registrazione. Per altre informazioni, vedere [Registrazione.](logging.md)                                                                            |
| DO   | Modalità di debug. Per altre informazioni, vedere [Eseguire il debug di](debug.md).                                                                                   |
| DI   | Disabilitare Windows programma di installazione. Per altre informazioni, vedere [DisableMsi.](disablemsi.md)                                                      |
| Wt   | Timeout di attesa in secondi in caso di assenza di attività. **HKLM** \\ **Software software** \\ **Criteri** \\ **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **Timeout** |
| DB   | Disabilitare l'esplorazione dei percorsi di origine da parte dell'utente. Per altre informazioni, vedere [DisableBrowse.](disablebrowse.md)                                     |
| Punto di distribuzione (DP)   | Disabilitare l'applicazione di patch. Per altre informazioni, vedere [DisablePatch.](disablepatch.md)                                                                |
| Uc   | Proprietà pubbliche inviate al servizio di installazione. Per altre informazioni, vedere [EnableUserControl.](enableusercontrol.md)                             |
| SS   | Programma di installazione sicuro per gli script dal browser. Per altre informazioni, vedere [SafeForScripting.](safeforscripting.md)                               |
| EM   | Privilegi di sistema (HKLM). Per altre informazioni, vedere [AlwaysInstallElevated.](alwaysinstallelevated.md)                                      |
| EU   | Privilegi di sistema (HKCU). Per altre informazioni, vedere [AlwaysInstallElevated.](alwaysinstallelevated.md)                                      |
| DR   | Disabilitare i criteri di rollback. Per altre informazioni, vedere [DisableRollback.](disablerollback.md)                                                   |
| TS   | Individuare le trasformazioni nella radice dell'immagine di origine. Per altre informazioni, vedere [TransformsAtSource policy (Criteri TransformsAtSource).](transformsatsource-policy.md)             |
| TP   | Aggiungere moduli sicuri nella cache lato client. Per altre informazioni, vedere [TransformsSecure policy](transformssecure-policy.md).                 |
| SO   | Ordine di ricerca dei tipi di origine. Per altre informazioni, vedere [SearchOrder.](searchorder.md)                                                      |



 

Per altri esempi di scripting, vedere Windows [di script del programma di installazione](windows-installer-scripting-examples.md). Per le utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 




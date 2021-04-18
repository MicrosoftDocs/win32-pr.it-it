---
description: Il file VBScript WiPolicy.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come utilizzare lo script per gestire i criteri di sistema. Il criterio può essere configurato da un amministratore utilizzando l'Editor Criteri di gruppo (GPE).
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Gestione delle impostazioni dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86684e75e09fa0a588c2d1d0d999488d6e89fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308182"
---
# <a name="manage-policy-settings"></a>Gestione delle impostazioni dei criteri

Il file VBScript WiPolicy.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per gestire i [criteri di sistema](system-policy.md). Il criterio può essere configurato da un amministratore utilizzando l'Editor Criteri di gruppo (GPE).

In questo esempio vengono illustrati i criteri di Windows Installer.

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**valore del \[ criterio WiPolicy.vbs cscript \] \[\]**

Se nella riga di comando non è specificato alcun argomento, nell'esempio vengono restituite le impostazioni dei criteri correnti. Specificare i criteri da impostare usando i codici identificatore seguenti. Specificare il nuovo valore per il criterio. Per restituire il valore corrente di un criterio, specificare una stringa vuota "" per il valore.



| CODE | Descrizione                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Modalità di registrazione. Per ulteriori informazioni, vedere [registrazione](logging.md) .                                                                            |
| DO   | Modalità di debug. Per ulteriori informazioni, vedere [debug](debug.md).                                                                                   |
| DI   | Disabilitare la modalità Windows Installer. Per ulteriori informazioni, vedere [DisableMsi](disablemsi.md).                                                      |
| WT   | Timeout di attesa in secondi in caso di assenza di attività. **HKLM** \\ **Software** \\ di **Criteri** \\ di **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **Timeout** |
| DB   | Disabilitare l'esplorazione utente dei percorsi di origine. Per ulteriori informazioni, vedere [DisableBrowse](disablebrowse.md).                                     |
| Punto di distribuzione (DP)   | Disabilitare l'applicazione di patch. Per ulteriori informazioni, vedere [DisablePatch](disablepatch.md).                                                                |
| UC   | Proprietà pubbliche inviate al servizio di installazione. Per ulteriori informazioni, vedere [EnableUserControl](enableusercontrol.md).                             |
| SS   | Programma di installazione sicuro per lo script dal browser. Per ulteriori informazioni, vedere [SafeForScripting](safeforscripting.md).                               |
| EM   | Privilegi di sistema (HKLM). Per ulteriori informazioni, vedere [AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| EU   | Privilegi di sistema (HKCU). Per ulteriori informazioni, vedere [AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| DR   | Disabilitare i criteri di rollback. Per ulteriori informazioni, vedere [DisableRollback](disablerollback.md).                                                   |
| TS   | Individuare le trasformazioni alla radice dell'immagine di origine. Per ulteriori informazioni, vedere [criteri di TransformsAtSource](transformsatsource-policy.md).             |
| TP   | Aggiungere trasforma protetti nella cache sul lato client. Per ulteriori informazioni, vedere [criteri di TRANSFORMSSECURE](transformssecure-policy.md).                 |
| SO   | Ordine di ricerca dei tipi di origine. Per ulteriori informazioni, vedere [SearchOrder](searchorder.md).                                                      |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 




---
description: Qualsiasi linguaggio di scripting, ad esempio VBScript, che funziona con ActiveX oggetti può accedere ai dati WMI. Le applicazioni possono accedere a WMI in C++, usando l'API COM per WMI o in Visual Basic, usando la libreria dei tipi Wbemdisp.tlb e l'API scripting per WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Creazione di un'applicazione o di uno script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddde26b2a8495126b4aa26c132adb49860627230d698431df5d713e653f1d874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412131"
---
# <a name="creating-a-wmi-application-or-script"></a>Creazione di un'applicazione o di uno script WMI

Qualsiasi linguaggio di scripting, ad esempio VBScript, che funziona con ActiveX oggetti può accedere ai dati WMI. Le applicazioni possono accedere a WMI in C++, usando [l'API COM](com-api-for-wmi.md) per WMI o in Visual Basic, usando la libreria dei tipi Wbemdisp.tlb e l'API scripting per [WMI](scripting-api-for-wmi.md). [](using-the-wmi-scripting-type-library.md) . È possibile ottenere dati tramite WMI scrivendo uno script, una Active Server (ASP) o un'applicazione HTML (HTA). È anche possibile usare Windows PowerShell per ottenere dati o scrivere script. Per altre informazioni, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) e Attività iniziali con [Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). TechNet ScriptCenter in [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contiene centinaia di esempi di scripting. Per altre informazioni sulle risorse di stampa e online, vedere [Altre informazioni](further-information.md).

La procedura seguente descrive come connettersi al servizio WMI e all'archivio dati.

**Per connettersi al servizio WMI e all'archivio dati**

1.  Individuare il servizio WMI in un computer specifico.
2.  Connessione a uno o più spazi dei nomi WMI.

Queste operazioni sono diverse nei linguaggi C++, Visual Basic, .NET Framework o quando si usa uno script. Gli script e Visual Basic applicazioni devono accedere alle classi le cui istanze vengono fornite con dati dai provider esistenti. Ma le applicazioni scritte in C++ possono fare di più. Ad esempio, un'applicazione scritta in C++ può inviare eventi, ma uno script WMI può sottoscrivere solo per ricevere eventi.

Un provider WMI può essere scritto solo in C++ o usando il .NET Framework. Per altre informazioni sulla scrittura di applicazioni in C# o Visual Basic .NET, vedere [Panoramica di WMI .NET.](/previous-versions/bb404655(v=vs.90))

Per altre informazioni sulla creazione di applicazioni e script per WMI, vedere:

-   [Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md)
-   [Creazione di uno script WMI](creating-a-wmi-script.md)
-   [Creazione di un client WMI gestito](creating-a-managed-wmi-client.md)

Per eseguire la maggior parte delle attività, usare le classi [WMI preinstallate](wmi-classes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di WMI](using-wmi.md)
</dt> </dl>

 

 

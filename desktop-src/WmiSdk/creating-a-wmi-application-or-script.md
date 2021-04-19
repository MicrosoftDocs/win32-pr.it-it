---
description: Qualsiasi linguaggio di scripting, ad esempio VBScript, che funziona con gli oggetti ActiveX può accedere ai dati WMI. Le applicazioni possono accedere a WMI in C++, usando l'API COM per WMI o in Visual Basic, usando la libreria dei tipi wbemdisp. tlb e l'API di scripting per WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Creazione di un'applicazione o di uno script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317563"
---
# <a name="creating-a-wmi-application-or-script"></a>Creazione di un'applicazione o di uno script WMI

Qualsiasi linguaggio di scripting, ad esempio VBScript, che funziona con gli oggetti ActiveX può accedere ai dati WMI. Le applicazioni possono accedere a WMI in C++, usando l' [API com per WMI](com-api-for-wmi.md) o in Visual Basic, usando la [libreria dei tipi](using-the-wmi-scripting-type-library.md) wbemdisp. tlb e l' [API di scripting per WMI](scripting-api-for-wmi.md). . È possibile ottenere dati tramite WMI scrivendo uno script, una pagina di Active Server (ASP) o un'applicazione HTML (HTA). È anche possibile usare Windows PowerShell per ottenere dati o scrivere script. Per ulteriori informazioni, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) e [Introduzione con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contiene centinaia di esempi di scripting. Per ulteriori informazioni sulle risorse di stampa e online, vedere [ulteriori informazioni](further-information.md).

Nella procedura riportata di seguito viene descritto come connettersi all'archivio dati e al servizio WMI.

**Per connettersi al servizio WMI e all'archivio dati**

1.  Individuare il servizio WMI in un computer specifico.
2.  Connettersi a uno o più spazi dei nomi WMI.

Queste operazioni sono diverse in C++, Visual Basic, .NET Framework linguaggi o quando si usa uno script. Gli script e le applicazioni Visual Basic devono accedere alle classi le cui istanze vengono fornite con i dati dai provider esistenti. Tuttavia, le applicazioni scritte in C++ possono eseguire altre operazioni. Ad esempio, un'applicazione scritta in C++ può inviare eventi, ma uno script WMI può solo sottoscrivere gli eventi di ricezione.

Un provider WMI può essere scritto solo in C++ o utilizzando il .NET Framework. Per ulteriori informazioni sulla scrittura di applicazioni in C# o Visual Basic .NET, vedere [Panoramica di WMI .NET](/previous-versions/bb404655(v=vs.90)).

Per ulteriori informazioni sulla creazione di applicazioni e script per WMI, vedere:

-   [Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md)
-   [Creazione di uno script WMI](creating-a-wmi-script.md)
-   [Creazione di un client WMI gestito](creating-a-managed-wmi-client.md)

Per eseguire la maggior parte delle attività, utilizzare le [classi WMI](wmi-classes.md)preinstallate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> </dl>

 

 

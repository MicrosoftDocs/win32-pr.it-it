---
description: Gli script possono accedere a tutte le classi WMI per gli oggetti hardware e software.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Scripting dell'accesso a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0169da5b2d7d9d542d7fe686ae34f5bf2aeb3c4fdfff1e268dc3ca2bfdddd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992391"
---
# <a name="scripting-access-to-wmi"></a>Scripting dell'accesso a WMI

Gli script possono accedere a tutte le classi WMI per gli oggetti hardware e software. Windows Gli script dell'host di script (WSH) possono eseguire operazioni file system oggetti, modificare le stampanti di rete o modificare le variabili di ambiente. È possibile trovare un'ampia gamma di attività di amministratore e brevi linee guida su come eseguire queste operazioni in WMI in [Wmi Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md). Per altre informazioni ed esempi, vedere il [repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)di script TechNet ScriptCenter.

Se non si ha di che creare script o di script specifici di WMI, vedere la sezione TechNet ScriptCenter [Attività iniziali](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).

Con [l'API di scripting per WMI](scripting-api-for-wmi.md)è possibile sviluppare script semplici e rapidi o applicazioni complesse. Lo scripting offre la stessa possibilità di ottenere informazioni o di configurare la maggior parte degli oggetti in un'azienda, come si farebbe con un'applicazione C++ o C#. Per altre informazioni, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Non è possibile scrivere [*un provider WMI*](gloss-p.md) nello script. Per altre informazioni, vedere [Fornire dati a WMI.](providing-data-to-wmi.md)

Gli script WMI possono essere scritti in qualsiasi linguaggio di scripting in grado di interagire con ActiveX oggetti.

Windows PowerShell un ambiente semplice per l'amministrazione WMI e lo scripting. Per altre informazioni su PowerShell, vedere [Attività iniziali con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

Gli script ADSI (Active Directory Service Interface) forniscono l'accesso Active Directory Domain Services oggetti (AD DS). Sia gli script WSH che gli script ADSI accedono agli oggetti e consentono procedure non disponibili tramite file batch.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 

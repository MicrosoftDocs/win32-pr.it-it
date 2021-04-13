---
description: Gli script possono accedere a tutte le classi WMI per gli oggetti hardware e software.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Creazione di script per l'accesso a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226829"
---
# <a name="scripting-access-to-wmi"></a>Creazione di script per l'accesso a WMI

Gli script possono accedere a tutte le classi WMI per gli oggetti hardware e software. Gli script di Windows script host (WSH) possono eseguire operazioni sugli oggetti file system, modificare le stampanti di rete o modificare le variabili di ambiente. È possibile trovare una serie di attività amministrative e brevi istruzioni su come eseguirle in WMI nelle [attività WMI per gli script e le applicazioni](wmi-tasks-for-scripts-and-applications.md). Per ulteriori informazioni ed esempi, vedere il repository di [script](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)TechNet ScriptCenter.

Se non si ha familiarità con lo scripting o con lo scripting specifico di WMI, vedere la sezione TechNet ScriptCenter [Introduzione](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).

Con l' [API di scripting per WMI](scripting-api-for-wmi.md)è possibile sviluppare script rapidi e semplici o applicazioni complesse. Lo scripting offre la stessa funzionalità per ottenere informazioni o per configurare la maggior parte degli oggetti in un'organizzazione come se si trattasse di un'applicazione C++ o C#. Per ulteriori informazioni, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Non è possibile scrivere un [*provider WMI*](gloss-p.md) nello script. Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).

Gli script WMI possono essere scritti in qualsiasi linguaggio di scripting in grado di interagire con gli oggetti ActiveX.

Windows PowerShell offre un ambiente semplice per l'amministrazione e lo script WMI. Per ulteriori informazioni su PowerShell, vedere [Introduzione con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

Gli script di Active Directory Service Interfaces (ADSI) forniscono l'accesso agli oggetti di Active Directory Domain Services (AD DS). Gli script WSH e ADSI accedono agli oggetti e consentono procedure non disponibili tramite file batch.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 

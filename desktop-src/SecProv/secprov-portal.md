---
description: I provider WMI per la sicurezza possono essere utilizzati per gli script WMI e per creare un provider di sicurezza gestito.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Provider WMI per la sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306376"
---
# <a name="security-wmi-providers"></a>Provider WMI per la sicurezza

## <a name="purpose"></a>Scopo

I provider WMI per la sicurezza consentono agli amministratori e ai programmatori di configurare Crittografia unità BitLocker (BDE) e il Trusted Platform Module (TPM) utilizzando Strumentazione gestione Windows (WMI).

## <a name="developer-audience"></a>Sviluppatori

In questo documento viene specificata l'interfaccia del provider WMI per la gestione e la configurazione di Crittografia unità BitLocker (BDE) e Trusted Platform Module (TPM) in Windows Server 2008 R2 e Windows Server 2008 per i server e Windows 7 e Windows Vista per i computer client. È concepita per essere letta da quelli che scrivono script, elementi dell'interfaccia utente o altri strumenti di amministrazione per BDE o TPM.

## <a name="run-time-requirements"></a>Requisiti di runtime

Per i provider WMI di sicurezza è necessario specificare il file con estensione MOF con ogni provider e un sistema operativo supportato. Il sistema operativo minimo è Windows Server 2008 o Windows Vista. Crittografia unità BitLocker è disponibile solo per le versioni Windows Vista Enterprise e Windows Vista Ultimate di Windows Vista. Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                               | Descrizione                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informazioni sui provider WMI per la sicurezza](about-security-wmi-providers.md)<br/>         | Breve panoramica dei provider WMI per la sicurezza.<br/>           |
| [Guida di riferimento ai provider WMI di sicurezza](security-wmi-providers-reference.md)<br/> | Documentazione di riferimento per i provider WMI per la sicurezza.<br/> |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Di seguito sono riportate altre risorse.



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classi<br/> | Per ulteriori informazioni sui provider WMI per la sicurezza, vedere [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) e [**Win32 \_ TPM**](win32-tpm.md).<br/> |



 

 

 





---
description: I provider WMI di sicurezza possono essere usati per lo scripting wmi e per creare un provider di sicurezza gestito.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Provider WMI di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d81833abff5160847678d094694702e4711de90
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581989"
---
# <a name="security-wmi-providers"></a>Provider WMI di sicurezza

## <a name="purpose"></a>Scopo

I provider WMI di sicurezza consentono agli amministratori e ai programmatori di configurare Crittografia unità BitLocker (BDE) e Trusted Platform Module (TPM) usando Windows Management Instrumentation (WMI).

## <a name="developer-audience"></a>Sviluppatori

Questo documento specifica l'interfaccia del provider WMI per la gestione e la configurazione di Crittografia unità BitLocker (BDE) e Trusted Platform Module (TPM) in Windows Server 2008 R2 e Windows Server 2008 per i server e Windows 7 e Windows Vista per i computer client. È destinato a essere letto da chi scrive script, elementi dell'interfaccia utente o altri strumenti di amministrazione per BDE o TPM.

## <a name="run-time-requirements"></a>Requisiti di runtime

I provider WMI di sicurezza richiedono il file mof specificato con ogni provider e un sistema operativo supportato. Il sistema operativo minimo è Windows Server 2008 o Windows Vista. Crittografia unità BitLocker è disponibile solo per le versioni Windows Vista Enterprise e Windows Vista Ultimate di Windows Vista. Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                               | Descrizione                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informazioni sui provider WMI di sicurezza](about-security-wmi-providers.md)<br/>         | Breve panoramica dei provider WMI di sicurezza.<br/>           |
| [Informazioni di riferimento per i provider WMI di sicurezza](security-wmi-providers-reference.md)<br/> | Documentazione di riferimento per i provider WMI di sicurezza.<br/> |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Di seguito sono riportate altre risorse.



| Risorsa     | Descrizione                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classi      | Per altre informazioni sui provider WMI di sicurezza, vedere [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) e [**Win32 \_ Tpm.**](win32-tpm.md) |



 

 

 





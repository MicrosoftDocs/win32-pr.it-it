---
description: Rimozione di WPDUSB.SYS driver per Windows dispositivi portatili
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Rimozione di WPDUSB.SYS driver per Windows dispositivi portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b5d1a815b97049816a618b9e93d0767e321fd60b689e6845318c1605574c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994741"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Rimozione di WPDUSB.SYS driver per Windows dispositivi portatili

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

Microsoft ha sostituito il componente in modalità kernel dello stack di driver USB di Windows Vista (WPDUSB.SYS) per dispositivi portabili Windows (WPD) con il driver WINUSB.SYS generico. La comunicazione con il driver WPDUSB.SYS originale era tramite codici di controllo I/O privati (IOCTL). Anche il supporto di questi elementi è stato rimosso.

Tutti i consumer di questi codici IOCTL sarebbero stati responsabili dell'interpretazione e dell'implementazione appropriate del protocollo MTP (Media Transfer Protocol). Windows Vista non supporta l'uso di questi codici IOCTL da parte di applicazioni di terze parti.

## <a name="manifestation-of-impact"></a>Impatto significativo

Qualsiasi applicazione che dipendeva dalla disponibilità di questi codici IOCTL privati non avrebbe più accesso ai dispositivi MTP connessi tramite USB.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli utenti di un'applicazione che dipende dai codici IOCTL privati devono usare un'applicazione diversa (o una versione aggiornata dell'applicazione) per accedere al dispositivo MTP connesso tramite USB.

## <a name="solution"></a>Soluzione

Le applicazioni devono usare Windows'API WPD (Portable Devices) per trovare e interagire con qualsiasi dispositivo WPD. Anche se una percentuale significativa di dispositivi WPD implementa MTP per la comunicazione con il PC, la WPD non è limitata ai soli dispositivi MTP. Inoltre, se l'accesso diretto al dispositivo tramite gli IOCL privati avrebbe limitato l'applicazione alla comunicazione solo con dispositivi connessi tramite USB, l'uso dell'API WPD espande l'elenco delle opzioni di connettività ad altri protocolli di comunicazione (ad esempio, Wi-Fi). Nei rari casi in cui l'applicazione deve essere in grado di riconoscere MTP, l'API WPD fornisce un meccanismo pass-through per i comandi MTP non elaborati.

## <a name="leveraging-feature-capabilities"></a>Uso delle funzionalità

L'API WPD è supportata in Windows XP (tramite Windows Format SDK), Windows Vista e Windows 7. L'Windows 7 di WPD aggiunge il supporto per MTP su Bluetooth.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

[Windows Dispositivi portatili](../windows-portable-devices.md)

 

 

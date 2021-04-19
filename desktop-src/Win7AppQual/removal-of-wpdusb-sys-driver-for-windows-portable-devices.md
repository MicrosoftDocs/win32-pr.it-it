---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Rimozione del driver WPDUSB.SYS per dispositivi portatili Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317611"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Rimozione del driver WPDUSB.SYS per dispositivi portatili Windows

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

Microsoft ha sostituito il componente modalità kernel dello stack di driver USB di Windows Vista (WPDUSB.SYS) per i dispositivi portatili Windows (WPD) con il driver di WINUSB.SYS generico. La comunicazione con il driver di WPDUSB.SYS originale è stata tramite codici IOCTL (private I/O Control); anche il supporto di questi elementi è stato rimosso.

Tutti i consumer di questi codici IOCTL sarebbero stati responsabili dell'interpretazione e dell'implementazione corrette del protocollo MTP (Media Transfer Protocol). Windows Vista non supportava l'utilizzo di questi codici IOCTL da parte di applicazioni di terze parti.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Qualsiasi applicazione che dipende dalla disponibilità di questi codici IOCTL privati non avrà più accesso ai dispositivi MTP connessi tramite USB.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli utenti di un'applicazione che dipende dai codici IOCTL privati devono usare un'applicazione diversa o una versione aggiornata dell'applicazione per accedere al dispositivo MTP connesso tramite USB.

## <a name="solution"></a>Soluzione

Per individuare e interagire con qualsiasi dispositivo WPD, le applicazioni devono usare l'API dispositivi portatili Windows (WPD). Sebbene una percentuale significativa di dispositivi WPD implementi MTP per la comunicazione con il PC, WPD non è limitato solo ai dispositivi MTP. Inoltre, quando l'accesso diretto al dispositivo tramite le IOCTL private avrebbe limitato l'applicazione alla comunicazione con solo i dispositivi connessi tramite USB, l'uso dell'API WPD espande l'elenco di opzioni di connettività ad altri protocolli di comunicazione, ad esempio Wi-Fi. Nei rari casi in cui l'applicazione deve essere compatibile con MTP, l'API WPD fornisce un meccanismo pass-through per i comandi MTP non elaborati.

## <a name="leveraging-feature-capabilities"></a>Sfruttando le funzionalità

L'API WPD è supportata in Windows XP (tramite Windows Format SDK), Windows Vista e Windows 7. L'implementazione di Windows 7 di WPD aggiunge il supporto per MTP su Bluetooth.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

[Dispositivi portatili Windows](../windows-portable-devices.md)

 

 

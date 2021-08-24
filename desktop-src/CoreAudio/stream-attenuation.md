---
description: Esperienza di analisi predefinita
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Esperienza di analisi predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec323bdaf01a7bba0821a9dee2c349239b3a53660334d2ac57edbf71287f396d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695017"
---
# <a name="default-ducking-experience"></a>Esperienza di analisi predefinita

Si consideri uno scenario in cui un utente riceve una chiamata telefonica durante l'ascolto di musica sul computer. Durante la chiamata telefonica, l'utente vuole ridurre il livello di volume della musica durante la chiamata telefonica e riprendere il volume originale al termine della chiamata telefonica. A seconda delle opzioni specificate dall'utente nel pannello di controllo  Suoni, il sistema operativo fornisce automaticamente questa funzionalità tramite attenuazione del flusso o di attenuazione del flusso, con riduzione dell'intensità di un flusso audio. 

L'esperienza di attenuazione predefinita dipende dalle preferenze dell'utente, come specificato nell'opzione Audio del pannello **di** controllo. Nella scheda **Comunicazioni** l'utente può scegliere un livello di attenuazione (il valore predefinito è 80%), disattivare tutti i flussi non di comunicazione o disabilitare l'esperienza di attenuazione del flusso predefinita. Il sistema consente l'apertura di nuovi flussi non di comunicazione (ad eccezione dei nuovi suoni di sistema) durante la sessione di comunicazione, ma i nuovi flussi non vengono attenuati automaticamente. Quando tutti i flussi di comunicazione vengono chiusi, il sistema termina la sessione di comunicazione e ripristina il volume dei flussi attenuati durante la sessione di comunicazione.

Per indicare visivamente l'attenuazione del flusso, il sistema modifica le impostazioni del mixer del volume in base alle preferenze dell'utente. Ad esempio, se l'utente specifica un livello di attenuazione, il mixer del volume abbassa il dispositivo di scorrimento, visualizza il nuovo volume attenuato e visualizza il livello del volume originale. L'immagine seguente illustra questo processo.

![Diagramma del comportamento di attenuazione del flusso predefinito fornito in Windows 7](images/stream-aatenuation.jpg)

Un'applicazione può eseguire l'override dell'attenuazione del flusso e implementare un'esperienza di controllo personalizzata se sa quando viene avviata e terminata la sessione di comunicazione. Per altre informazioni, vedere [Providing a Custom Papering Behavior](providing-a-custom-ducking-experience.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un dispositivo di comunicazione](using-the-communication-device.md)
</dt> <dt>

[Disabilitazione dell'esperienza di analisi predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornire un comportamento personalizzato per l'accodamento](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per l'accodamento delle notifiche](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Recupero di eventi di antartide](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 




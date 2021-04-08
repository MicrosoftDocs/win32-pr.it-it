---
description: Esperienza di ducking predefinita
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Esperienza di ducking predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748530"
---
# <a name="default-ducking-experience"></a>Esperienza di ducking predefinita

Si consideri uno scenario in cui un utente riceve una telefonata mentre ascolta la musica del computer. Durante la telefonata, l'utente desidera ridurre il livello di volume della musica mentre partecipa alla telefonata e riprendere il volume originale al termine della telefonata. A seconda delle opzioni specificate dall'utente nel pannello di controllo **Sounds** , il sistema operativo fornisce automaticamente questa funzionalità tramite l' *attenuazione del flusso* o l' *abbassamento* di flusso, riducendo l'intensità di un flusso audio.

L'esperienza di attenuazione predefinita dipende dalle preferenze dell'utente, come specificato nell'opzione **Sound** del pannello di controllo. Nella scheda **comunicazioni** l'utente può scegliere un livello di attenuazione (il valore predefinito è 80%), disattivare tutti i flussi non di comunicazione o disabilitare l'esperienza di attenuazione del flusso predefinita. Il sistema consente l'apertura di nuovi flussi non di comunicazione (ad eccezione dei nuovi suoni di sistema) durante la sessione di comunicazione, ma i nuovi flussi non vengono attenuati automaticamente. Quando tutti i flussi di comunicazione vengono chiusi, il sistema termina la sessione di comunicazione e ripristina il volume dei flussi che sono stati attenuati durante la sessione di comunicazione.

Per indicare visivamente l'attenuazione del flusso, il sistema modifica le impostazioni del mixer del volume a seconda delle preferenze dell'utente. Ad esempio, se l'utente specifica un livello di attenuazione, il mixer del volume abbassa il dispositivo di scorrimento, Visualizza il nuovo volume attenuato e visualizza il livello del volume originale. Questo processo è illustrato nella figura seguente.

![diagramma del comportamento di attenuazione del flusso predefinito disponibile in Windows 7](images/stream-aatenuation.jpg)

Un'applicazione può eseguire l'override dell'attenuazione del flusso e implementare un'esperienza di ducking personalizzata se sa quando inizia e termina la sessione di comunicazione. Per altre informazioni, vedere [fornire un comportamento di ducking personalizzato](providing-a-custom-ducking-experience.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un dispositivo di comunicazione](using-the-communication-device.md)
</dt> <dt>

[Disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornire un comportamento di ducking personalizzato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Recupero di eventi ducking](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 




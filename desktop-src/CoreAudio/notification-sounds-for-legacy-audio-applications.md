---
description: Suoni di notifica per le applicazioni audio legacy
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Suoni di notifica per le applicazioni audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523802"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a>Suoni di notifica per le applicazioni audio legacy

In Windows Vista, il sistema operativo assegna tutti i suoni di notifica del sistema a una sessione audio tra processi che riproduce il dispositivo dell'endpoint di rendering che è attualmente assegnato al ruolo del [dispositivo](device-roles.md)eConsole. Il programma di controllo del volume di sistema, sndvol, Visualizza un dispositivo di scorrimento del volume dedicato ai suoni delle notifiche di sistema.

Alcune applicazioni riprodotno i suoni di notifica. Anziché richiedere all'utente di gestire le notifiche di un'applicazione tramite un dispositivo di scorrimento del volume separato in sndvol, l'applicazione può assegnare i suoni di notifica alla stessa sessione del suono delle notifiche di sistema. Il dispositivo di scorrimento del volume sndvol che controlla i suoni della notifica di sistema controlla quindi i suoni di notifica dall'applicazione.

Per abilitare questo comportamento, Windows Vista definisce un \_ flag di sistema SND per la funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) legacy. Questo flag non è supportato nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000. Se il chiamante imposta questo flag, la funzione **PlaySound** assegna il suono che riproduce alla sessione tra processi utilizzata dal sistema operativo per i suoni di notifica. Se il chiamante non imposta il flag, **PlaySound** assegna il suono che riproduce alla sessione predefinita, ovvero la sessione specifica del processo identificata dal GUID del valore GUID della sessione \_ null. \_Il sistema SND è definito nel file di intestazione MMSYSTEM. h. Per ulteriori informazioni su **PlaySound**, vedere la documentazione Windows SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interoperabilità con le API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 

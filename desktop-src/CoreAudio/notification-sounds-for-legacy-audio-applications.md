---
description: Segnali acustici di notifica per applicazioni audio legacy
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Segnali acustici di notifica per applicazioni audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce813fb2d38a9995f929c62936879f502392415d040e88ddb50f3b4699734a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077525"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a>Segnali acustici di notifica per applicazioni audio legacy

In Windows Vista, il sistema operativo assegna tutti i suoni di notifica di sistema a una sessione audio tra processi che [](device-roles.md)viene riprodotta tramite il dispositivo endpoint di rendering attualmente assegnato al ruolo del dispositivo eConsole . Il programma di controllo del volume di sistema, Sndvol, visualizza un dispositivo di scorrimento del volume dedicato ai suoni di notifica del sistema.

Alcune applicazioni riproduceno suoni di notifica. Invece di richiedere all'utente di gestire i suoni di notifica di un'applicazione tramite un dispositivo di scorrimento del volume separato in Sndvol, l'applicazione può assegnare i suoni di notifica alla stessa sessione dei suoni delle notifiche di sistema. Il dispositivo di scorrimento del volume Sndvol che controlla i suoni delle notifiche di sistema controlla quindi i suoni di notifica dall'applicazione.

Per abilitare questo comportamento, Windows Vista definisce un flag SND \_ SYSTEM per la funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) legacy. Questo flag non è supportato nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000. Se il chiamante imposta questo flag, la funzione **PlaySound** assegna il suono riprodotto alla sessione tra processi utilizzata dal sistema operativo per i suoni di notifica. Se il chiamante non imposta il flag, **PlaySound** assegna il suono riprodotto alla sessione predefinita, ovvero la sessione specifica del processo identificata dal valore GUID DELLA sessione \_ NULL. SND \_ SYSTEM è definito nel file di intestazione Mmsystem.h. Per altre informazioni su **PlaySound,** vedere la documentazione Windows SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interoperabilità con LE API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 

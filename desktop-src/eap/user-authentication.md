---
title: Autenticazione degli utenti
description: Il protocollo di autenticazione stesso può autenticare l'utente tramite PEAP (Protected EAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3f5d377163f2519d97de847d8d14b5bd96925577a8133988adf8fbf950b283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978371"
---
# <a name="user-authentication"></a>Autenticazione degli utenti

Il protocollo di autenticazione stesso può autenticare l'utente tramite PEAP (Protected EAP). Nel sistema operativo sono inoltre incorporati due provider di autenticazione: l'autenticazione Windows dominio (a cui si accede tramite Servizi directory) e radiuS (Remote Access Dial-In User Service).

Nel caso in cui RADIUS sia il provider di autenticazione, il plug-in EAP viene installato nel server RADIUS anziché nel server del punto di accesso wireless, ad esempio un server RAS. Il server AP passa i pacchetti EAP direttamente dal client al servizio di autenticazione nel server RADIUS. Il server AP non elabora alcuna informazione nei pacchetti EAP, ma deve accettare le chiavi di crittografia generate da PEAP sul lato server e a livello completo (256 bit) per creare la connessione protetta.

 

 





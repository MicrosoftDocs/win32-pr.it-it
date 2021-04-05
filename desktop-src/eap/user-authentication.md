---
title: Autenticazione degli utenti
description: Il protocollo di autenticazione può autenticare l'utente tramite PEAP (Protected EAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719570"
---
# <a name="user-authentication"></a>Autenticazione degli utenti

Il protocollo di autenticazione può autenticare l'utente tramite PEAP (Protected EAP). Sono inoltre disponibili due provider di autenticazione integrati nel sistema operativo: autenticazione del dominio di Windows (a cui si accede tramite servizi directory) e servizio di accesso remoto (RADIUS, Remote Access Dial-in User).

Nel caso in cui RADIUS sia il provider di autenticazione, il plug-in EAP viene installato nel server RADIUS anziché nel server punto di accesso wireless, ad esempio un server RAS. Il server AP passa i pacchetti EAP direttamente dal client al servizio di autenticazione sul server RADIUS. Il server AP non elabora alcuna informazione nei pacchetti EAP, ma deve accettare le chiavi di crittografia generate dal lato server, complete (256 bit), per creare la connessione protetta.

 

 





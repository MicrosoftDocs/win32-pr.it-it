---
title: Parametro animazione area client
description: Il flag di animazione dell'area client indica se l'utente desidera disabilitare le animazioni negli elementi dell'interfaccia utente.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224017"
---
# <a name="client-area-animation-parameter"></a>Parametro animazione area client

Il parametro animazione area client indica se l'utente desidera disabilitare le animazioni negli elementi dell'interfaccia utente. Le funzionalità di visualizzazione, ad esempio il lampeggio, il lampeggio, lo sfarfallio e lo stato del contenuto possono causare convulsioni negli utenti con epilessia sensibile alle foto. Questo parametro consente di abilitare o disabilitare tutte le animazioni di questo tipo.

Le applicazioni usano i flag **SPI \_ GETCLIENTAREAANIMATION** e **SPI \_ SETCLIENTAREAANIMATION** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per attivare o disattivare le animazioni dell'area client.

 

 
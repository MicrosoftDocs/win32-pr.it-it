---
title: Parametro di animazione dell'area client
description: Il flag di animazione dell'area client indica se l'utente vuole disabilitare le animazioni negli elementi dell'interfaccia utente.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4d451424da0a02fa55efaead05ab285b3f07936167bb6e4376de4fd25ae11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325960"
---
# <a name="client-area-animation-parameter"></a>Parametro di animazione dell'area client

Il parametro di animazione dell'area client indica se l'utente vuole disabilitare le animazioni negli elementi dell'interfaccia utente. Le funzionalità di visualizzazione, ad esempio flashing, lampeggiamento, sfarfallio e spostamento del contenuto, possono causare problemi agli utenti con epilessia sensibile alle foto. Questo parametro consente di abilitare o disabilitare tutte queste animazioni.

Le applicazioni usano i flag **SPI \_ GETCLIENTAREAANIMATION** e **SPI \_ SETCLIENTAREAANIMATION** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per attivare o disattivare le animazioni dell'area client.

 

 
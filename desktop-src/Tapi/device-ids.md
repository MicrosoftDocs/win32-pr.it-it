---
description: Altre funzioni telefoniche TAPI usano un handle per un dispositivo telefono aperto per identificare il dispositivo telefono aperto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: ID dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51363d5b5de2ee45858c5500231ef2b9840087160574e9884958fb724328932e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867393"
---
# <a name="device-ids"></a>ID dei dispositivi

Altre funzioni telefoniche TAPI usano un handle per un dispositivo telefono aperto per identificare il dispositivo telefono aperto. Le uniche funzioni per i dispositivi telefonici che accettano un parametro dell'identificatore di dispositivo telefono (anziché un handle del telefono) sono le funzioni [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneOpen.**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) Un'applicazione può recuperare l'identificatore di dispositivo del telefono usando la [**funzione phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) con l'handle del telefono come parametro.

Un'applicazione può anche ottenere gli identificatori di dispositivo per varie classi di dispositivi associate a un telefono aperto richiamando [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid). Per i nomi delle classi di dispositivo, vedere Classi di dispositivi [TAPI.](tapi-device-classes.md)

Questa funzione accetta un handle del telefono e una descrizione della classe del dispositivo. Restituisce l'identificatore di dispositivo per il dispositivo della classe di dispositivo specificata associata al dispositivo telefono aperto. Se la classe del dispositivo è "tapi/phone", viene restituito l'identificatore del dispositivo telefonico.

A differenza dei dispositivi di linea, per i quali i servizi di linea di base forniscono l'equivalente di POTS, non è definito alcun set minimo di funzioni garantite per i dispositivi telefonici. Anche se ogni dispositivo telefonico fornisce almeno le funzioni e i messaggi descritti in questa sezione, non offrono operazioni effettive sul dispositivo fisico.

 

 




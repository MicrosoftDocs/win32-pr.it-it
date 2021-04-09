---
description: Le classi di dispositivi semplificano lo sviluppo consentendo ai programmatori di trattare i dispositivi con proprietà simili in modo analogo.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Classe Device (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967471"
---
# <a name="device-class"></a>Classe Device

Le classi di dispositivi semplificano lo sviluppo consentendo ai programmatori di trattare i dispositivi con proprietà simili in modo analogo. Un telefono digitale in un ufficio, ad esempio, ha in genere più funzionalità rispetto a un portatile standard in una casa, ma entrambi rispondono allo stesso modo a un set di funzioni di base ed entrambi appartengono a una classe di dispositivi telefonici. Le classi di dispositivi consentono di rendere TAPI estendibile offrendo un Framework da cui classificare e supportare nuove apparecchiature.

Vedere [le classi di dispositivi TAPI](./tapi-device-classes.md) per le classi che TAPI ha predefinito. Un provider di servizi può implementare e definire classi di dispositivi aggiuntive per le apparecchiature supportate. Un'applicazione non deve mai essere in grado di individuare il provider di servizi che controlla il dispositivo, ma può richiedere informazioni sul controllo delle nuove classi del dispositivo.

Un provider di servizi implementa una classe dispositivo eseguendo il mapping delle richieste ai comandi del dispositivo effettivi. Ad esempio, quando il provider di servizi per un modem compatibile con Hayes riceve un comando passato tramite TAPISVR per effettuare una chiamata, invia i comandi classici al modem.

L'interfaccia del provider di servizi può essere mappata a un'ampia gamma di ambienti, inclusi quelli non tradizionalmente considerati come appartenenti alla telefonia. Un esempio è la conferenza multimediale su una rete basata su IP, ad esempio Internet.

Gli sviluppatori di applicazioni devono tenere in considerazione l'esistenza di altre applicazioni che possono condividere servizi di telefonia.

 

 

---
description: TAPI assegna gli identificatori di sessione univoci per ogni sessione e applicazione.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificatore session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527706159328b3919e47c39bc5fb160615ed2c202d33c1ce39c711b6921235a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760783"
---
# <a name="session-identifier"></a>Identificatore session

TAPI assegna gli identificatori di sessione univoci per ogni sessione e applicazione. Un'applicazione usa un identificatore di sessione per comunicare con TAPI relativo a una sessione specifica. Un'applicazione ottiene in genere un identificatore creando una nuova sessione di comunicazione o quando TAPI offre una sessione.

Non è possibile usare un identificatore di sessione per passare informazioni a un'altra applicazione. A questo scopo, usare [l'ID chiamata](call-id-ovr.md), che può essere assegnato da un provider di servizi.

Per [informazioni sulle operazioni che](initiate-a-session-ovr.md) creano sessioni e restituiscono un identificatore di sessione, vedere Avviare una sessione. Vedere [Rispondere alla sessione avviata altrove per le](respond-to-session-initiated-elsewhere-ovr.md) operazioni che acquisiscono gli identificatori di sessione da TAPI. Per [informazioni sul rilascio delle risorse di](terminate-a-session-ovr.md) sessione, vedere Terminare una sessione.

Tutti i provider di servizi devono supportare una qualche forma di identificazione della sessione.

**TAPI 2.x:** L'identificatore principale di una sessione di comunicazione è l'handle di chiamata.

**TAPI 3.x:** Una sessione è rappresentata da un [oggetto call e](call-object.md) l'identificatore primario è un puntatore [**all'interfaccia ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

 

 




---
description: TAPI assegna gli identificatori di sessione univoci per ogni sessione e applicazione.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificatore session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401800"
---
# <a name="session-identifier"></a>Identificatore session

TAPI assegna gli identificatori di sessione univoci per ogni sessione e applicazione. Un'applicazione usa un identificatore di sessione per comunicare con TAPI per una sessione specifica. Un'applicazione ottiene in genere un identificatore creando una nuova sessione di comunicazione o quando TAPI offre una sessione.

Impossibile utilizzare un identificatore di sessione per passare informazioni a un'altra applicazione. A questo scopo, usare l' [ID chiamata](call-id-ovr.md), che può essere assegnato da un provider di servizi.

Vedere [avviare una sessione](initiate-a-session-ovr.md) per informazioni sulle operazioni che creano sessioni e restituiscono un identificatore di sessione. Vedere [rispondere a una sessione avviata altrove](respond-to-session-initiated-elsewhere-ovr.md) per le operazioni che acquisiscono gli identificatori di sessione da TAPI. Per informazioni sul rilascio delle risorse della sessione, vedere [terminare una sessione](terminate-a-session-ovr.md) .

Tutti i provider di servizi devono supportare una forma di identificazione della sessione.

**TAPI 2. x:** L'identificatore primario di una sessione di comunicazione è l'handle di chiamata.

**TAPI 3. x:** Una sessione è rappresentata da un [oggetto chiamata](call-object.md) e l'identificatore primario è un puntatore all'interfaccia [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

 

 




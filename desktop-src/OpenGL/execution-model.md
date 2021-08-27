---
title: Modello di esecuzione
description: Modello di esecuzione
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modello di esecuzione
- Modello di esecuzione OpenGL
- OpenGL, modello client/server
- Modello client/server OpenGL
- OpenGL, trasparente per la rete
- framebuffers, modello di esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7cb7c3c06baa0a56f4c59b14744b73962fced369d56f00cbf887b9ae6d09e2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082461"
---
# <a name="execution-model"></a>Modello di esecuzione

Il modello per l'interpretazione dei comandi OpenGL è client/server. Il codice dell'applicazione (client) genera comandi che vengono interpretati ed elaborati da OpenGL (server). Il server può funzionare o meno nello stesso computer del client. In questo senso, OpenGL è trasparente per la rete. Un server può gestire diversi contesti OpenGL, ognuno dei quali è uno stato OpenGL incapsulato. Un client può connettersi a uno di questi contesti. Il protocollo di rete richiesto può essere implementato aumentando un protocollo già esistente (ad esempio quello del sistema X Window) o usando un protocollo indipendente. Non vengono forniti comandi OpenGL per ottenere l'input dell'utente.

Il sistema di finestre che alloca le risorse framebuffer controlla infine gli effetti dei comandi OpenGL sul framebuffer. Sistema di finestre:

-   Determina a quali parti del framebuffer OpenGL può accedere in qualsiasi momento.
-   Comunica a OpenGL come sono strutturate queste parti.

Pertanto, non sono disponibili comandi OpenGL per configurare framebuffer o inizializzare OpenGL. La configurazione del buffer dei frame viene eseguita all'esterno di OpenGL in combinazione con il sistema della finestra. L'inizializzazione OpenGL viene attivata quando il sistema della finestra alloca una finestra per il rendering OpenGL.

 

 





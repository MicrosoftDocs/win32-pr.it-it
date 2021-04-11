---
title: Modello di esecuzione
description: Modello di esecuzione
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modello di esecuzione
- modello di esecuzione OpenGL
- OpenGL, modello client/server
- modello client/server OpenGL
- OpenGL, trasparente per la rete
- framebuffer, modello di esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955731"
---
# <a name="execution-model"></a>Modello di esecuzione

Il modello per l'interpretazione dei comandi OpenGL è client/server. Il codice dell'applicazione (il client) rilascia i comandi, che vengono interpretati ed elaborati da OpenGL (il server). Il server può funzionare o meno nello stesso computer del client. In questo senso, OpenGL è trasparente per la rete. Un server può gestire diversi contesti OpenGL, ciascuno dei quali è uno stato di OpenGL incapsulato. Un client può connettersi a uno di questi contesti. Il protocollo di rete richiesto può essere implementato aumentando un protocollo già esistente, ad esempio quello del sistema Windows X, oppure usando un protocollo indipendente. Non è stato fornito alcun comando OpenGL per ottenere l'input dell'utente.

Il sistema Windows che alloca le risorse framebuffer controlla infine gli effetti dei comandi OpenGL sul framebuffer. Sistema Windows:

-   Determina a quali parti del framebuffer OpenGL può accedere in un determinato momento.
-   Comunica con OpenGL come sono strutturate le parti.

Non sono pertanto disponibili comandi OpenGL per la configurazione del framebuffer o l'inizializzazione di OpenGL. La configurazione del buffer dei frame viene eseguita all'esterno di OpenGL insieme al sistema Windows; L'inizializzazione di OpenGL viene eseguita quando il sistema della finestra alloca una finestra per il rendering OpenGL.

 

 





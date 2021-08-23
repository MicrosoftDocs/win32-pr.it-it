---
description: Se un thread è in attesa del completamento di un callback in modalità kernel, il lato modalità utente del thread ritarda una chiamata alla funzione ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Rilevamento di Kernel-Mode callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029ecf7d5b1f9220de51c2ecffe4bdf30da4cbd088d9d251fd0d24bab04934e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691451"
---
# <a name="detecting-kernel-mode-callbacks"></a>Rilevamento di Kernel-Mode callback

La maggior parte del codice per l'Windows del sistema operativo viene eseguita in modalità kernel. La modalità processore passa dalla modalità utente alla modalità kernel ogni volta che un thread dell'applicazione chiama una funzione dall'API Windows che a sua volta chiama una funzione di sistema interna che deve essere eseguita in modalità kernel. La modalità processore torna alla modalità utente prima che il controllo restituisca alla funzione in modo che i dati di sistema sono protetti.

Se un thread è in attesa del completamento di un callback in modalità kernel, il lato modalità utente del thread ritarda una chiamata alla **funzione ZwCallbackReturn.**

 

 




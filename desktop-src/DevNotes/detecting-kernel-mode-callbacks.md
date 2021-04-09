---
description: Se un thread è in attesa del completamento di un callback in modalità kernel, il lato della modalità utente del thread ritarderà a una chiamata alla funzione ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Rilevamento di callback di Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966246"
---
# <a name="detecting-kernel-mode-callbacks"></a>Rilevamento di callback di Kernel-Mode

La maggior parte del codice per il sistema operativo Windows viene eseguita in modalità kernel. La modalità processore passa dalla modalità utente alla modalità kernel ogni volta che un thread dell'applicazione chiama una funzione dall'API Windows che a sua volta chiama una funzione di sistema interna che deve essere eseguita in modalità kernel. La modalità processore torna alla modalità utente prima che il controllo venga restituito alla funzione in modo che i dati di sistema siano protetti.

Se un thread è in attesa del completamento di un callback in modalità kernel, il lato della modalità utente del thread ritarderà a una chiamata alla funzione **ZwCallbackReturn** .

 

 




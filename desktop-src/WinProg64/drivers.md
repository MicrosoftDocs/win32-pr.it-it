---
title: Driver (Guida per programmatori per la versione a 64 bit Windows)
description: La versione a 64 bit di Windows è progettata per consentire agli sviluppatori di usare una singola base di codice sorgente per le applicazioni a 32 bit e a 64 bit. In gran parte, questo vale anche per i driver a 32 bit e a 64 bit Windows driver.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- driver a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cda928bbfc8c7f83e3aeac0bacbaea1e1a46214d9c0785d4675a3042b87fa1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132854"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Driver (Guida per programmatori per la versione a 64 bit Windows)

La versione a 64 bit di Windows è progettata per consentire agli sviluppatori di usare una singola base di codice sorgente per le applicazioni a 32 bit e a 64 bit. In gran parte, questo vale anche per i driver a 32 bit e a 64 bit Windows driver.

Tuttavia, i driver a 32 bit non possono essere eseguiti in Windows a 64 bit e devono essere portati. Per le applicazioni in modalità utente, il Windows a 64 bit include WOW64, che consente alle applicazioni Windows a 32 bit di essere eseguite (con una certa perdita di prestazioni) nei sistemi che eseguono applicazioni Windows a 64 bit. Non esiste alcun livello di conversione equivalente per i driver.

Per informazioni sulla portabilità dei driver in Windows a 64 bit, vedere [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) (Problemi a 64 bit) in Windows Driver Kit (WDK).

 

 





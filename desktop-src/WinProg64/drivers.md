---
title: Driver (Guida per programmatori per Windows a 64 bit)
description: La versione a 64 bit di Windows è progettata per consentire agli sviluppatori di usare un'unica base di codice sorgente per le applicazioni a 32 bit e 64 bit. In larga misura, questo vale anche per i driver Windows a 32 bit e a 64 bit.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- driver programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340212"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Driver (Guida per programmatori per Windows a 64 bit)

La versione a 64 bit di Windows è progettata per consentire agli sviluppatori di usare un'unica base di codice sorgente per le applicazioni a 32 bit e 64 bit. In larga misura, questo vale anche per i driver Windows a 32 bit e a 64 bit.

Tuttavia, i driver a 32 bit non possono essere eseguiti su Windows a 64 bit e devono essere trasportati. Per le applicazioni in modalità utente, Windows a 64 bit include WOW64, che consente l'esecuzione di applicazioni Windows a 32 bit (con alcune perdite di prestazioni) sui sistemi che eseguono Windows a 64 bit. Non esiste alcun livello di conversione equivalente per i driver.

Per informazioni sul porting dei driver in Windows a 64 bit, vedere [problemi relativi a 64 bit](https://msdn.microsoft.com/library/aa489627.aspx) in Windows Driver Kit (WDK).

 

 





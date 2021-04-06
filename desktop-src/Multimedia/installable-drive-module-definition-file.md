---
title: File di Module-Definition unità installabile
description: File di Module-Definition unità installabile
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- driver installabili, file di definizione moduli
- driver installabili, file DEF
- driver nstallable, funzione DriverProc
- DriverProc (funzione)
- file di definizione moduli
- DEF (file)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046633"
---
# <a name="installable-drive-module-definition-file"></a>File di Module-Definition unità installabile

La definizione di modulo (. DEF) il file di un driver installabile assegna un nome al driver, Esporta la funzione [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) e definisce una descrizione del driver. Nell'esempio seguente viene illustrato un file di definizione dei moduli tipico per un driver installabile:


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



Alcune applicazioni di installazione possono aprire il driver e recuperare la riga di descrizione da usare durante l'installazione del driver. Per mantenere la compatibilità con queste applicazioni di installazione, la riga della descrizione deve avere il formato seguente:

**Descrizione**  *alias* \[ ,*alias* \] ... **:* * * testo*

L' *alias* specifica un nome univoco per il driver che può essere utilizzato dalle applicazioni per aprire il driver. L'alias funge anche da nome del valore associato al driver nel registro di sistema. Più alias sono separati da virgole. Il *testo* descrive lo scopo del driver.

 

 
---
title: Variabili per l'esecuzione dell'elaborazione
description: Variabili per l'esecuzione dell'elaborazione
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, elaborazione di variabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711107"
---
# <a name="variables-to-perform-processing"></a>Variabili per l'esecuzione dell'elaborazione

Le variabili membro per la gestione del buffer di ritardo occupano le quantità di **byte** ; si tratta di puntatori a **byte** e di un numero intero che archivia un conteggio di byte. Questa soluzione è ideale per l'elaborazione di audio a 8 bit, perché un campione a 8 bit si adatta perfettamente a un byte di memoria. Quando si elaborano audio a 16 bit, tuttavia, è più comodo convertirli in puntatori **brevi** , in modo che l'elaborazione possa essere eseguita due byte alla volta.

Il codice di esempio seguente alloca i nuovi puntatori a 16 bit e aggiunge una variabile puntatore che archivia l'indirizzo della fine del buffer di ritardo. Inserirlo nella sezione "Case 16" immediatamente prima del punto di ingresso del ciclo:


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



Il codice per l'elaborazione a 8 bit consente inoltre di allocare una variabile che archivia l'indirizzo della fine del buffer di ritardo. L'archiviazione di questo valore rende più semplice verificare se il puntatore del buffer dei ritardi mobili ha raggiunto la fine del buffer di ritardo. Il codice di esempio seguente calcola il valore:


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





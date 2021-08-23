---
title: Variabili per gestire il buffer di ritardo
description: Variabili per gestire il buffer di ritardo
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Windows Media Player plug-in, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione del segnale digitale, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
- Esempio di plug-in Echo DSP, buffer di ritardo
- buffer di ritardo
- buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be71bc7f2ded34dcd5f29bc10ce01796b6498d36a9a194a48b0bfdec0e14662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571741"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Variabili per gestire il buffer di ritardo

È necessario aggiungere le dichiarazioni per le variabili membro necessarie per gestire il buffer di ritardo. Aggiungere le dichiarazioni seguenti a Echo.h nella sezione "private":


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



Aggiungere il codice seguente al costruttore CEcho per inizializzare le variabili del buffer di ritardo:


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso delle risorse di streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 





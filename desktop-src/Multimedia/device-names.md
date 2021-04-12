---
title: Nomi dei dispositivi
description: Nomi dei dispositivi
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471766"
---
# <a name="device-names"></a>Nomi dei dispositivi

Per ogni tipo di dispositivo potrebbero essere presenti diversi driver MCI che condividono il set di comandi ma operano su formati di dati diversi. Per identificare in modo univoco un driver MCI, MCI USA *i nomi di dispositivo*.

I nomi dei dispositivi sono identificati \[ nella \] sezione MCI del file SYSTEM.INI o nella parte appropriata del registro di sistema. Queste informazioni identificano tutti i driver MCI per Windows. Le voci nella \[ sezione MCI \] usano il formato seguente:

*\_ nome dispositivo*  =  *driver \_ filename. Extension*

Nell'esempio seguente viene illustrata \[ una \] sezione MCI tipica da SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Se un driver MCI viene installato usando un nome di dispositivo già esistente in SYSTEM.INI o nel registro di sistema, il sistema aggiunge un numero intero al nome del dispositivo del nuovo driver, creando un nome univoco per il dispositivo. Nell'esempio precedente, a un driver aggiuntivo installato con il nome del dispositivo "CDAudio" viene assegnato il nome del dispositivo "cdaudio1".

 

 





---
title: Nomi dei dispositivi
description: Nomi dei dispositivi
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85183a1b23817352ba9e45e8dbb2aaa70493430cd092f357e1eaa8e9bf179d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497271"
---
# <a name="device-names"></a>Nomi dei dispositivi

Per ogni tipo di dispositivo, potrebbero essere presenti diversi driver MCI che condividono il set di comandi ma operano su formati di dati diversi. Per identificare in modo univoco un driver MCI, MCI usa i *nomi di dispositivo*.

I nomi dei dispositivi vengono identificati nella sezione mci del \[ file SYSTEM.INI o nella parte appropriata del Registro di \] sistema. Queste informazioni identificano tutti i driver MCI da Windows. Le voci nella sezione \[ mci \] usano il formato seguente:

*device \_ name*  =  *driver \_ filename.extension*

L'esempio seguente illustra una \[ tipica sezione mci \] di SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Se un driver MCI viene installato usando un nome di dispositivo già esistente in SYSTEM.INI o nel Registro di sistema, il sistema aggiunge un numero intero al nome del dispositivo del nuovo driver, creando un nome di dispositivo univoco. Nell'esempio precedente, a un driver aggiuntivo installato con il nome del dispositivo "cdaudio" viene assegnato il nome del dispositivo "cdaudio1".

 

 





---
description: Definisce gli intervalli di data e ora con un formato simile alla sintassi di data e ora suddividendo la stringa nei campi per giorni, ore, minuti, secondi e microsecondi.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato intervallo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318873"
---
# <a name="interval-format"></a>Formato intervallo

WMI definisce gli intervalli di data e ora con un formato simile alla sintassi di data e ora suddividendo la stringa nei campi per giorni, ore, minuti, secondi e microsecondi.

Nell'esempio seguente viene illustrato il formato di un intervallo di data e ora.

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

Nella tabella seguente sono elencati i campi dell'intervallo di data/ora.



| Campo    | Descrizione                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dddddddd | Otto cifre che rappresentano un numero di giorni (da 00000000 a 99999999).                                                                                                                                                                    |
| HH       | Ora del giorno a due cifre che utilizza il formato a 24 ore (da 00 a 23).                                                                                                                                                                       |
| MM       | Minuto a due cifre nell'ora (da 00 a 59).                                                                                                                                                                                                |
| SS       | Numero di secondi di due cifre nel minuto (da 00 a 59).                                                                                                                                                                                   |
| mmmmmm   | Numero di microsecondi a sei cifre nel secondo (da 000000 a 999999). L'implementazione non è necessaria per supportare la valutazione con questo campo, ma questo campo deve essere sempre presente per mantenere la natura a lunghezza fissa della stringa. |



 

Gli intervalli hanno sempre una ": 000" finale come gli ultimi quattro caratteri. A differenza di data e ora, inoltre, non è possibile utilizzare asterischi per indicare i campi inutilizzati. Inoltre, tutte le proprietà di tipo [CIM \_ DateTime](cim-datetime.md) che rappresentano gli intervalli devono essere contrassegnate con il qualificatore standard del [sottotipo](standard-wmi-qualifiers.md) , con il qualificatore impostato su "Interval".

La stringa seguente rappresenta un intervallo di 1 giorno, 12 ore, 0 minuti e 32 secondi.

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato di data e ora](date-and-time-format.md)
</dt> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[\_DateTime CIM](cim-datetime.md)
</dt> </dl>

 

 




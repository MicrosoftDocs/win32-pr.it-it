---
description: Se questo bit è impostato per un controllo testo statico, il controllo tenta automaticamente di formattare il testo visualizzato come numero che rappresenta un conteggio di byte.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Attributo di controllo FormatSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226615"
---
# <a name="formatsize-control-attribute"></a>Attributo di controllo FormatSize

Se questo bit è impostato per un controllo testo statico, il controllo tenta automaticamente di formattare il testo visualizzato come numero che rappresenta un conteggio di byte. Per una corretta formattazione, il testo del controllo deve essere impostato su una stringa che rappresenta un numero espresso in unità di 512 byte. Il valore visualizzato viene quindi formattato in kilobyte (KB), megabyte (MB) o gigabyte (GB) e visualizzato con la stringa appropriata che rappresenta le unità. Per altre informazioni, vedere [controllo testo](text-control.md).



| Valore numerico del testo originale | Stringa di unità utilizzata |
|----------------------------------|------------------|
| Minore di 20480                  | KB               |
| Minore di 20971520               | MB               |
| Minore di 10737418240            | GB               |



 

## <a name="valid-controls"></a>Controlli validi



| Decimal | Valore esadecimale | Control                          |
|---------|-------------|----------------------------------|
| 524288  | 0x00080000  | msidbControlAttributesFormatSize |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere i bit FormatSize nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md). Il testo del controllo deve essere impostato su una stringa che rappresenta un numero espresso in unità di 512 byte. Il testo delle stringhe di unità viene definito nella [tabella UIText](uitext-table.md). Il posizionamento della stringa di unità è controllato dalla proprietà [**LeftUnit**](leftunit.md) . Se la proprietà **LeftUnit** è definita come qualsiasi valore, la stringa di unità viene visualizzata prima del valore numerico. Se nel testo associato al controllo è presente un valore diverso da caratteri numerici, il valore visualizzato non è definito.

In fase di esecuzione, il programma di installazione risolve la proprietà [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) nel numero totale di byte necessari per l'installazione in unità di 512. Un controllo testo statico con bit FormatSize può essere usato per formattare automaticamente ed etichettare il numero totale di byte necessari per l'installazione in KB, MB o GB, a seconda dei casi. Ai fini di questo esempio, si supponga che il numero totale di byte sia 18.336.768. Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRequired su 18.336.768 diviso per 512 o 35.814. Il numero visualizzato dal controllo testo con FormatSize è 17MB.

I valori numerici del testo originale sono espressi in unità di 512. Nella tabella precedente la stringa 20.480 corrisponde alla stringa KB perché 20.480 volte 512 restituisce un risultato di 10.485.760 byte o 10.240 KB.

Le stringhe di unità elencate nella tabella precedente si riferiscono alle chiavi della [tabella UIText](uitext-table.md), in cui è definito il testo della stringa di unità.

Il posizionamento della stringa di unità è controllato dalla proprietà [**LeftUnit**](leftunit.md) . Se la proprietà **LeftUnit** è definita come qualsiasi valore, la stringa di unità viene visualizzata prima del valore numerico.

Se nel testo associato al controllo è presente un valore diverso da caratteri numerici, il valore visualizzato non è definito.

Per altre informazioni, vedere [controllare gli attributi](control-attributes.md) e i [controlli](controls.md).

 

 




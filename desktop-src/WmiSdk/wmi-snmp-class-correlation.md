---
description: La correlazione influiscono sul set di classi restituite da archivio SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Correlazione della classe SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226936"
---
# <a name="wmi-snmp-class-correlation"></a>Correlazione della classe SNMP WMI

La correlazione influiscono sul set di classi restituite da archivio SMIR. Le classi correlate sono quelle che un determinato dispositivo SNMP è in grado di supportare nel momento in cui si verifica l'enumerazione. L'enumerazione non correlata restituisce tutte le classi presenti all'interno di archivio SMIR, indipendentemente dal fatto che siano supportate dal dispositivo. La correlazione è una funzionalità del provider SNMP WMI e può essere disattivata o attivata (impostazione predefinita).

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

La correlazione potrebbe impedire la visualizzazione di tutte le classi effettivamente supportate da un dispositivo. Se è noto che una determinata classe è supportata, ma non viene visualizzata in archivio SMIR, questo può essere dovuto a diversi motivi, uno dei quali è la correlazione. Prendere in considerazione la disattivazione della correlazione prima di scrivere nel dispositivo in questione. Tuttavia, la disattivazione della correlazione comporta la probabilità che molte classi non supportate dal dispositivo vengano visualizzate in archivio SMIR. Inoltre, l'utilizzo della correlazione comporta un costo in termini di prestazioni, in quanto viene eseguita una query sul dispositivo per vedere quali classi sono supportate. Quando la correlazione è attivata, il provider SNMP causa un'enumerazione delle classi supportate dal dispositivo in modo analogo al risultato dell'esecuzione di uno strumento di *percorso MIB* .

Un gestore reti, ad esempio, vuole conoscere diversi elementi chiave di dati relativi a tutti gli hub gestiti in una determinata rete. Un database dei dispositivi correnti e del relativo MIB supportato esiste già, pertanto non è necessario basarsi sulla funzione di correlazione del dispositivo per fornire gli elementi dati supportati. In questo caso, la correlazione potrebbe essere disattivata.

Nell'esempio seguente viene illustrato come disattivare la correlazione.


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



D'altra parte, un altro gestore reti potrebbe voler monitorare tutte le unità disco del computer UNIX sulla rete, ma non ha familiarità con i dati MIB in tali computer. In tal caso, la correlazione verrebbe attivata.

 

 




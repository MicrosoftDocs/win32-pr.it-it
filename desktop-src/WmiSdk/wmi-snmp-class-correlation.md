---
description: La correlazione influisce sul set di classi restituite da SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Correlazione della classe SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d795b7e998e3b7392baa45c23d688f1a2cef6a4069f6671d4c209788e7c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815704"
---
# <a name="wmi-snmp-class-correlation"></a>Correlazione della classe SNMP WMI

La correlazione influisce sul set di classi restituite da SMIR. Le classi correlate sono quelle supportate da un determinato dispositivo SNMP al momento dell'enumerazione. L'enumerazione non correlata restituisce tutte le classi presenti all'interno di SMIR, indipendentemente dal fatto che il dispositivo le supporti. La correlazione è una funzionalità del provider SNMP WMI e può essere disattivata o attivata (impostazione predefinita).

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Configurazione dell'ambiente SNMP WMI.](setting-up-the-wmi-snmp-environment.md)

 

La correlazione potrebbe impedire la visualizzazione di tutte le classi effettivamente supportate da un dispositivo. Se si sa che una classe specifica è supportata ma non viene visualizzata in SMIR, ciò potrebbe essere dovuto a diversi motivi, uno dei quali è la correlazione. Provare a disattivare la correlazione prima di scrivere nel dispositivo in questione. Tuttavia, la disattivazione della correlazione comporta la probabilità che molte classi non supportate dal dispositivo vengano visualizzate in SMIR. Inoltre, l'uso della correlazione ha un costo in termini di prestazioni perché viene eseguita una query sul dispositivo per visualizzare le classi supportate. Quando la correlazione è attivata, il provider SNMP genera un'enumerazione di classi supportate dal dispositivo simile al risultato dell'esecuzione di uno strumento di analisi *mib.*

Ad esempio, un gestore di rete vuole conoscere diversi dati chiave su tutti gli hub gestiti in una particolare rete. Esiste già un database dei dispositivi correnti e dei relativi MIB supportati, quindi non è necessario affidarsi alla funzione di correlazione del dispositivo per fornire gli elementi di dati supportati. In questo caso, la correlazione potrebbe essere disattivata.

Nell'esempio seguente viene illustrato come disattivare la correlazione.


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



D'altra parte, un altro gestore di rete potrebbe voler monitorare tutte le unità disco del computer UNIX in rete, ma non ha familiarità con i dati MIB in tali computer. In tal caso, la correlazione sarebbe attivata.

 

 




---
title: Valori restituiti dalla funzione WinSNMP
description: Il valore restituito da una chiamata di funzione WinSNMP può essere un handle per una risorsa allocata dall'implementazione di Microsoft WinSNMP per l'applicazione WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047238"
---
# <a name="winsnmp-function-return-values"></a>Valori restituiti dalla funzione WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Il valore restituito da una chiamata di funzione WinSNMP può essere un handle per una risorsa allocata dall'implementazione di Microsoft WinSNMP per l'applicazione WinSNMP.

Nella tabella seguente sono elencati i cinque tipi di handle di risorsa allocati dall'implementazione.



| Tipo di handle    | Descrizione                       |
|----------------|-----------------------------------|
| \_sessione HSNMP | Handle per una sessione WinSNMP       |
| \_entità HSNMP  | Handle per un'entità SNMP          |
| \_contesto HSNMP | Handle per un contesto SNMP         |
| \_PDU HSNMP     | Handle per un'unità dati del protocollo    |
| \_VBL HSNMP     | Handle per un elenco di associazioni variabili |



 

Per altre informazioni, vedere [oggetti handle di risorsa](resource-handle-objects.md).

Il valore restituito può essere anche un valore long integer senza segno del tipo **smiUINT32** che rappresenta un \_ valore di stato snmpapi.

Nella tabella seguente sono elencati i valori di stato di WinSNMP e il relativo significato.



| Stato           | Descrizione                                                                      |
|------------------|----------------------------------------------------------------------------------|
| \_errore snmpapi | Indica un errore. Equivale a 0 o **null**.                                    |
| SNMPAPI \_ riuscito | Indica che la funzione è stata completata correttamente. Equivale a 1 o a un conteggio positivo. |



 

 

 
---
title: Codici di errore WinSNMP
description: Codici di errore WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- WinSNMP codici di errore SNMP
- Codici di errore SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473966"
---
# <a name="winsnmp-error-codes"></a>Codici di errore WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

> [!Note]  
> Gli errori descritti in questo argomento sono distinti dai codici di errore SNMP definiti dalle RFC pertinenti.

 

Tutte le funzioni WinSNMP restituiscono il valore **snmpapi \_ Failure** se la funzione ha esito negativo. L'applicazione WinSNMP deve chiamare immediatamente la funzione [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) per recuperare le informazioni estese sugli errori quando una funzione WinSNMP ha esito negativo. Nella tabella seguente sono elencati gli argomenti che illustrano i codici di errore estesi restituiti dalle funzioni WinSNMP.



| Argomento                                                        | Descrizione                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Codici di errore comuni di WinSNMP](winsnmp-common-error-codes.md) | Vengono descritti i codici di errore comuni per l'API WinSNMP.       |
| [Errori di trasporto di rete](network-transport-errors.md)     | Descrive gli errori di trasporto di rete per l'API WinSNMP. |



 

Gli errori WinSNMP che comportano informazioni specifiche del contesto sono inclusi nella pagina di riferimento per le funzioni.

 

 
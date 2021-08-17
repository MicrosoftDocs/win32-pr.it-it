---
title: Codici di errore WinSNMP
description: Codici di errore WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Codici di errore WinSNMP SNMP
- Codici di errore SNMP , WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2a9f9dda792008a0e69e6c23e692b4aa4c4e78316eeca015f7b056e2a275df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142864"
---
# <a name="winsnmp-error-codes"></a>Codici di errore WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

> [!Note]  
> Gli errori descritti in questo argomento sono diversi dai codici di errore SNMP definiti dalle RFC pertinenti.

 

Tutte le funzioni WinSNMP restituiscono il valore **SNMPAPI \_ FAILURE se** la funzione ha esito negativo. L'applicazione WinSNMP deve chiamare immediatamente la [**funzione SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) per recuperare informazioni estese sugli errori quando una funzione WinSNMP ha esito negativo. Nella tabella seguente sono elencati gli argomenti che illustrano i codici di errore estesi restituiti dalle funzioni WinSNMP.



| Argomento                                                        | Descrizione                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Codici di errore comuni WinSNMP](winsnmp-common-error-codes.md) | Descrive i codici di errore comuni per l'API WinSNMP.       |
| [Errori di trasporto di rete](network-transport-errors.md)     | Descrive gli errori di trasporto di rete per l'API WinSNMP. |



 

Gli errori WinSNMP che trasmettono informazioni specifiche del contesto sono inclusi nella pagina di riferimento della funzione.

 

 
---
title: Gestione di un elenco di associazioni di variabili
description: La funzione SnmpGetVb recupera le informazioni sull'associazione di variabili da un elenco di associazioni di variabili. La funzione recupera il nome della variabile e il valore associato della variabile dalla voce di associazione della variabile specificata dall'applicazione WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c382e2780ae49a1f029aab2cfef2bcd4357fcfbf7b37ce9a1fcad9aed5bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009449"
---
# <a name="managing-a-variable-binding-list"></a>Gestione di un elenco di associazioni di variabili

La [**funzione SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera le informazioni sull'associazione di variabili da un elenco di associazioni di variabili. La funzione recupera il nome della variabile e il valore associato della variabile dalla voce di associazione della variabile specificata dall'applicazione WinSNMP.

Per aggiornare le voci di associazione di variabili in un elenco di associazioni di variabili, chiamare la [**funzione SnmpSetVb.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) La **funzione SnmpSetVb** aggiunge anche nuove voci di associazione di variabili a un elenco di associazioni di variabili esistente.

L'applicazione WinSNMP deve chiamare la [**funzione SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) per rimuovere voci da un elenco di associazioni di variabili.

Per recuperare, modificare o eliminare una voce di associazione di variabili, l'applicazione WinSNMP deve specificare la posizione della voce nell'elenco di binding delle variabili.

Una chiamata alla [**funzione SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associa un elenco di associazioni di variabili a una PDU. Una chiamata alla [**funzione SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera un elenco di associazioni di variabili da una PDU. Una singola associazione di variabili non è direttamente associata a una PDU, ma viene associata indirettamente tramite la relativa inclusione in un elenco di associazioni di variabili.

 

 





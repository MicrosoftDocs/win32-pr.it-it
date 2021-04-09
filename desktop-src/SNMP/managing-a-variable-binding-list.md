---
title: Gestione di un elenco di associazioni variabili
description: La funzione SnmpGetVb recupera le informazioni di associazione variabili da un elenco di associazioni variabili. La funzione recupera il nome della variabile e il valore associato della variabile dalla voce di associazione della variabile specificata dall'applicazione WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044467"
---
# <a name="managing-a-variable-binding-list"></a>Gestione di un elenco di associazioni variabili

La funzione [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera le informazioni di associazione variabili da un elenco di associazioni variabili. La funzione recupera il nome della variabile e il valore associato della variabile dalla voce di associazione della variabile specificata dall'applicazione WinSNMP.

Per aggiornare le voci di associazione variabili in un elenco di associazioni variabili, chiamare la funzione [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) . La funzione **SnmpSetVb** aggiunge anche nuove voci di associazione di variabili a un elenco di associazioni variabili esistente.

È necessario che l'applicazione WinSNMP chiami la funzione [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) per rimuovere le voci da un elenco di associazioni variabili.

Per recuperare, modificare o eliminare una voce di binding variabile, l'applicazione WinSNMP deve specificare la posizione della voce nell'elenco di associazioni variabili.

Una chiamata alla funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associa un elenco di associazioni variabili a una PDU. Una chiamata alla funzione [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera un elenco di associazioni variabili da un PDU. Un binding di una singola variabile non è associato direttamente a una PDU, ma è indirettamente associato tramite la relativa inclusione in un elenco di associazioni variabili.

 

 





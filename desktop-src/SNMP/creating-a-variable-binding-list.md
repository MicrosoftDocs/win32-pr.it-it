---
title: Creazione di un elenco di associazioni variabili
description: La funzione SnmpCreateVbl crea un nuovo elenco di associazioni di variabili.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221554"
---
# <a name="creating-a-variable-binding-list"></a>Creazione di un elenco di associazioni variabili

La funzione [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crea un nuovo elenco di associazioni di variabili. Se l'applicazione WinSNMP specifica un nome di variabile e un valore, la funzione crea l'elenco e aggiunge il nome e il valore come prima voce nell'elenco. Se l'applicazione specifica **null** come nome della variabile, la funzione crea un elenco vuoto.

Per copiare un elenco di associazioni di variabili, chiamare la funzione [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . La funzione crea un nuovo elenco di associazioni di variabili e inizializza il nuovo elenco con una copia dei dati nell'elenco di associazioni della variabile di origine.

La funzione [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e la funzione [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) allocano la memoria necessaria per il nuovo elenco di associazioni di variabili. L'applicazione WinSNMP deve rilasciare le risorse associate a questi elenchi. È consigliabile eseguire questa operazione eseguendo la corrispondenza di ogni chiamata a [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) con una chiamata corrispondente alla funzione [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) quando è opportuno liberare la memoria allocata.

 

 





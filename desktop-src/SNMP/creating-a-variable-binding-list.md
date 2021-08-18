---
title: Creazione di un elenco di associazioni di variabili
description: La funzione SnmpCreateVbl crea un nuovo elenco di associazioni di variabili.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2530b59524375ad6413ff9aa1416db8e25ee3641136284cb4a0f70795e388a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009579"
---
# <a name="creating-a-variable-binding-list"></a>Creazione di un elenco di associazioni di variabili

La [**funzione SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crea un nuovo elenco di associazioni di variabili. Se l'applicazione WinSNMP specifica un nome di variabile e un valore, la funzione crea l'elenco e aggiunge il nome e il valore come prima voce nell'elenco. Se l'applicazione specifica **NULL per** il nome della variabile, la funzione crea un elenco vuoto.

Per copiare un elenco di associazioni di variabili, chiamare la [**funzione SnmpDuplicateVbl.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) La funzione crea un nuovo elenco di associazioni di variabili e inizializza il nuovo elenco con una copia dei dati nell'elenco di associazione delle variabili di origine.

La [**funzione SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e la [**funzione SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) allocano la memoria necessaria per il nuovo elenco di associazioni di variabili. L'applicazione WinSNMP deve rilasciare le risorse associate a questi elenchi. È consigliabile che l'applicazione eserciti questa operazione abbinando ogni chiamata a [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) con una chiamata corrispondente alla [**funzione SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) quando è appropriato liberare la memoria allocata.

 

 





---
title: Aggiornamento di una PDU
description: Un'applicazione WinSNMP può recuperare e aggiornare i campi PDU selezionati usando le funzioni SnmpGetPduData e SnmpSetPduData.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713336"
---
# <a name="updating-a-pdu"></a>Aggiornamento di una PDU

Un'applicazione WinSNMP può recuperare e aggiornare i campi PDU selezionati usando le funzioni [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) e [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

L'applicazione può recuperare i campi tipo PDU, identificatore richiesta, stato errore e indice errore da una PDU specifica. Può anche recuperare l'handle per l'elenco di associazioni variabili. L'applicazione può aggiornare i **campi \_ tipo PDU** e **\_ ID richiesta** .

Se il tipo PDU è uguale a SNMP \_ PDU \_ GetBulk, l'applicazione può anche aggiornare i **non \_ ripetitori** e i campi **numero massimo \_** di ripetizioni della PDU.

 

 





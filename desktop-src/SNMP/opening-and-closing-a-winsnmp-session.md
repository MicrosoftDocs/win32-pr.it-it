---
title: Apertura e chiusura di una sessione WinSNMP
description: Per aprire una sessione, un'applicazione chiama la funzione SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41871c9adc2f7fcefc04b5816b29685ad6b1516a6238c1855ed41e878d5b2736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009199"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Apertura e chiusura di una sessione WinSNMP

Per aprire una sessione, un'applicazione chiama la [**funzione SnmpCreateSession.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) Se la funzione viene completata correttamente, l'implementazione Microsoft WinSNMP apre una sessione e la funzione restituisce un identificatore di sessione sotto forma di handle **HSNMP \_ SESSION.** Tutte le funzioni WinSNMP che restituiscono variabili handle includono l'identificatore di sessione come parametro di input. In questo modo l'implementazione di può usare l'handle per gestire in modo efficiente le risorse a livello di sessione.

Un'applicazione può avere più sessioni aperte contemporaneamente. Più sessioni all'interno di un'applicazione possono condividere variabili di gestione.

Se l'implementazione non può aprire una sessione a causa di limitazioni delle risorse, restituisce SNMPAPI FAILURE quando l'applicazione \_ chiama [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession). Se l'applicazione chiama quindi la [**funzione SnmpGetLastError,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) restituisce SNMPAPI \_ ALLOC \_ ERROR.

Una chiamata alla [**funzione SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) consente all'implementazione di liberare le risorse rimanenti e di chiudere la sessione.

Per altre informazioni, vedere [Oggetti handle di risorsa](resource-handle-objects.md) e Sessioni [WinSNMP.](winsnmp-sessions.md)

 

 





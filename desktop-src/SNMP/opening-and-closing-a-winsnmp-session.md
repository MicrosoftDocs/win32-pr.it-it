---
title: Apertura e chiusura di una sessione WinSNMP
description: Per aprire una sessione, un'applicazione chiama la funzione SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045038"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Apertura e chiusura di una sessione WinSNMP

Per aprire una sessione, un'applicazione chiama la funzione [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) . Se la funzione viene completata correttamente, l'implementazione di Microsoft WinSNMP apre una sessione e la funzione restituisce un identificatore di sessione sotto forma di handle **di \_ sessione HSNMP** . Tutte le funzioni WinSNMP che restituiscono variabili di handle includono l'identificatore di sessione come parametro di input. Questo consente all'implementazione di usare l'handle per gestire in modo efficiente le risorse a livello di sessione.

Un'applicazione può avere più sessioni aperte alla volta. Più sessioni all'interno di un'applicazione possono condividere le variabili di handle.

Se l'implementazione non è in grado di aprire una sessione a causa di limitazioni delle risorse, restituisce un \_ errore snmpapi quando l'applicazione chiama [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession). Se l'applicazione chiama la funzione [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , viene restituito un \_ errore di allocazione snmpapi \_ .

Una chiamata alla funzione [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) consente all'implementazione di liberare tutte le risorse rimanenti e di chiudere la sessione.

Per altre informazioni, vedere [oggetti handle di risorsa](resource-handle-objects.md) e [sessioni WinSNMP](winsnmp-sessions.md).

 

 





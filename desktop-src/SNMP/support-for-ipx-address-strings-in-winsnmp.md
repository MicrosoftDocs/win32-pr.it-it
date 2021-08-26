---
title: Supporto per le stringhe di indirizzo IPX in WinSNMP
description: WinSNMP 2.0 formalizza l'uso di stringhe di indirizzi IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: debd25897c32515b880ff82f691aa0421af6358ae72c7e49de3408d55bcbd609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886081"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Supporto per le stringhe di indirizzo IPX in WinSNMP

WinSNMP 2.0 formalizza l'uso di stringhe di indirizzi IPX. Se si specifica una stringa di indirizzo IPX come parametro di input per la [**funzione SnmpStrToEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) è necessario formattare la stringa usando gli standard seguenti:

-   Numero di rete costituito da otto cifre esadecimali (con riempimento zero se necessario)
-   Un separatore (":", "." o " – ")
-   Numero di nodo costituito da 12 cifre esadecimali (con riempimento zero se necessario)

Ad esempio, 00000001:00081A0D01C2 o 00000001.00081a0d01c2. Le cifre esadecimali possono essere maiuscole o minuscole.

Questo è il formato utilizzato [**dalla funzione SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) per restituire una stringa di indirizzo IPX. La stringa viene restituita quando un'applicazione che opera in una delle modalità SNMPAPI UNTRANSLATED chiama la \_ **funzione SnmpEntityToStr.** La stringa può essere restituita anche quando l'applicazione funziona in modalità SNMPAPI TRANSLATED e non è disponibile alcun nome descrittivo \_ per l'entità.

 

 





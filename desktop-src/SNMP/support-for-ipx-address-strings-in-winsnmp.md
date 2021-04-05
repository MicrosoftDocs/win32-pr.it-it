---
title: Supporto per le stringhe di indirizzi IPX in WinSNMP
description: WinSNMP 2,0 formalizza l'uso di stringhe di indirizzi IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707312"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Supporto per le stringhe di indirizzi IPX in WinSNMP

WinSNMP 2,0 formalizza l'uso di stringhe di indirizzi IPX. Se si specifica una stringa di indirizzo IPX come parametro di input per la funzione [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , è necessario formattare la stringa usando gli standard seguenti:

-   Numero di rete costituito da otto cifre esadecimali, se necessario con riempimento zero
-   Separatore (":", "." o "-")
-   Numero di nodo costituito da 12 cifre esadecimali, se necessario con riempimento zero

Ad esempio, 00000001:00081A0D01C2 o 00000001.00081 a0d01c2. Le cifre esadecimali possono essere maiuscole o minuscole.

Si tratta del formato utilizzato dalla funzione [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) per restituire una stringa di indirizzo IPX. La stringa viene restituita quando un'applicazione che opera in una delle modalità SNMPAPI non \_ tradotta chiama la funzione **SnmpEntityToStr** . La stringa può essere restituita anche quando l'applicazione funziona in \_ modalità snmpapi tradotta e non è disponibile alcun nome descrittivo per l'entità.

 

 





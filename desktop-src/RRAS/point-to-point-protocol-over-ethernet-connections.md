---
title: Point-to-Point Protocol over Ethernet connessioni
description: Windows Server 2003, Windows XP e sistemi operativi successivi forniscono il supporto per Point-to-Point Protocol over Ethernet (PPPoE). Per una connessione PPPoE, impostare i valori seguenti nella struttura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92703bac13d129ed29cee1c22328825de67325239c1906c1728b96d53398647b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789811"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>Point-to-Point Protocol over Ethernet connessioni

Windows Server 2003, Windows XP e sistemi operativi successivi forniscono il supporto per Point-to-Point Protocol over Ethernet (PPPoE). Per una connessione PPPoE, impostare i valori seguenti nella [**struttura RASENTRY.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))



| Membro                      | Valore             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | RASET \_ Broadband  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | Nome del servizio. |



 

Usare la [**funzione RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare questi valori.

È anche possibile usare [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) e il flag RASEDFLAG \_ NewBroadbandEntry per [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) per visualizzare una procedura guidata per la creazione di una voce della phonebook PPPoE.

 

 
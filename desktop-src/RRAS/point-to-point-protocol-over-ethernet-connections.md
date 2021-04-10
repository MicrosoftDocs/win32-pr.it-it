---
title: Point-to-Point Protocol su connessioni Ethernet
description: Windows Server 2003, Windows XP e i sistemi operativi successivi offrono il supporto per Point-to-Point Protocol su Ethernet (PPPoE). Per una connessione PPPoE, impostare i valori seguenti nella struttura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963383"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>Point-to-Point Protocol su connessioni Ethernet

Windows Server 2003, Windows XP e i sistemi operativi successivi offrono il supporto per Point-to-Point Protocol su Ethernet (PPPoE). Per una connessione PPPoE, impostare i valori seguenti nella struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Membro                      | Valore             |
|-----------------------------|-------------------|
| RASENTRY. dwType             | RASET \_ Broadband  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | Nome del servizio. |



 

Per impostare questi valori, usare la funzione [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) .

È anche possibile usare [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) e il \_ flag RASEDFLAG NewBroadbandEntry per [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) per visualizzare una procedura guidata per la creazione di una voce della rubrica PPPoE.

 

 
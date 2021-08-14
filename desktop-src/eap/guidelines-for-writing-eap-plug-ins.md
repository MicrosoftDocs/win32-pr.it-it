---
title: Linee guida per la scrittura di DLL EAP
description: È possibile scrivere DLL o plug-in EAP per ottimizzarne le prestazioni in scenari diversi.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c786da1ca026039ffd052f1213b2904dbfa602ee67c6d74aed7a0fe11fd9d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499156"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Linee guida per la scrittura di DLL EAP

È possibile scrivere DLL o plug-in EAP per ottimizzarne le prestazioni in scenari diversi.

## <a name="general-guidelines"></a>Linee guida generali

-   Per creare una connessione crittografata, i plug-in EAP devono generare chiavi di crittografia e restituirle tramite gli attributi RADIUS MS-MPPE-Send-Keys e MS-MPPE-Recv-Keys specifici del fornitore Microsoft. Per altre informazioni, vedere la sezione Osservazioni in [**\_ PPP EAP \_ OUTPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)

## <a name="wireless-guidelines"></a>Linee guida wireless

Di seguito sono riportate linee guida e raccomandazioni per la scrittura di un plug-in EAP che supporta l'autenticazione di computer in scenari wireless (802.1X). Questa sezione non si applica agli scenari VPN e dial-up.

-   Per non bloccare l'esecuzione automatica dei sistemi, i plug-in EAP non devono effettuare chiamate all'interfaccia utente.
-   L'implementazione del plug-in EAP del passaggio di autenticazione del computer deve essere completata il più rapidamente possibile, in modo da non ostacolare l'avvio del sistema operativo.
    > [!Note]  
    > Se il protocollo EAP non supporta l'autenticazione del computer, deve verificare la presenza del flag di autenticazione del computer, **RAS \_ EAP \_ FLAG MACHINE \_ \_ AUTH** usato nel campo **fFlags** in [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)e restituire un errore.

     

 

 





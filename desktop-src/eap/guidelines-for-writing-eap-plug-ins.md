---
title: Linee guida per la scrittura di DLL EAP
description: È possibile scrivere dll EAP o plug-in per ottimizzare le prestazioni in scenari diversi.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299293"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Linee guida per la scrittura di DLL EAP

È possibile scrivere dll EAP o plug-in per ottimizzare le prestazioni in scenari diversi.

## <a name="general-guidelines"></a>Linee guida generali

-   Per creare una connessione crittografata, è necessario che i plug-in EAP generino le chiavi di crittografia e le restituiscano tramite gli attributi RADIUS specifici del fornitore Microsoft MS-MPPE-send-keys e MS-MPPE-ricezione-Keys. Per ulteriori informazioni, vedere la sezione osservazioni nell' [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .

## <a name="wireless-guidelines"></a>Linee guida wireless

Di seguito sono riportate le linee guida e le indicazioni per la scrittura di un plug-in EAP che supporti l'autenticazione di computer in scenari wireless (802.1 X). Questa sezione non si applica a scenari VPN e remote.

-   Per non bloccare l'esecuzione di sistemi automatici, i plug-in EAP non devono effettuare chiamate all'interfaccia utente.
-   L'implementazione del plug-in EAP del passaggio di autenticazione del computer deve essere completata il più rapidamente possibile, in modo da non ostacolare l'avvio del sistema operativo.
    > [!Note]  
    > Se il protocollo EAP non supporta l'autenticazione del computer, deve verificare il flag di autenticazione del computer, l'autenticazione del **computer del \_ \_ flag EAP \_ \_ RAS** usato nel campo **fFlags** nell' [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)e restituire un errore.

     

 

 





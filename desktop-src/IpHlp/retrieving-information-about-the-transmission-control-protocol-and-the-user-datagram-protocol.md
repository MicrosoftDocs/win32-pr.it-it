---
description: L'helper IP consente di accedere alle informazioni sui protocolli di rete usati nel computer locale.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recupero di informazioni sul Transmission Control Protocol e sul protocollo di datagramma utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f10691c39e1f1a2c9c92af8736549427f01cc2400773e214f3a4d5f536fa46e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102051"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Recupero di informazioni sul Transmission Control Protocol e sul protocollo di datagramma utente

L'helper IP consente di accedere alle informazioni sui protocolli di rete usati nel computer locale. Utilizzare le funzioni descritte nei paragrafi seguenti per recuperare informazioni sul Transmission Control Protocol (TCP) e sul protocollo UDP (User Datagram Protocol) nel computer locale.

La [**funzione GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera le statistiche correnti per TCP. Per esempi di codice **che coinvolgono GetTcpStatistics,** vedere [Recupero di informazioni tramite GetTcpStatistics.](retrieving-information-using-gettcpstatistics.md)

La [**funzione GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera le statistiche correnti per UDP.

La [**funzione GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera la tabella di connessione TCP. [**GetUdpTable recupera**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) la tabella del listener UDP.

La [**funzione SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) consente a uno sviluppatore di impostare lo stato di una connessione TCP specificata su MIB \_ TCP STATE DELETE \_ \_ \_ TCB.

 

 




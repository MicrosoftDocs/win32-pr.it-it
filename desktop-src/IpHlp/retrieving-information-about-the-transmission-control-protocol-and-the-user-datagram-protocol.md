---
description: L'helper IP consente di accedere alle informazioni sui protocolli di rete utilizzati nel computer locale.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recupero di informazioni sul Transmission Control Protocol e sul protocollo del datagramma utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760844"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Recupero di informazioni sul Transmission Control Protocol e sul protocollo del datagramma utente

L'helper IP consente di accedere alle informazioni sui protocolli di rete utilizzati nel computer locale. Utilizzare le funzioni descritte nei paragrafi seguenti per recuperare informazioni sul Transmission Control Protocol (TCP) e sul protocollo UDP (User Datagram Protocol) nel computer locale.

La funzione [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera le statistiche correnti per TCP. Per esempi di codice che coinvolgono **GetTcpStatistics** , vedere [recupero di informazioni con GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).

La funzione [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera le statistiche correnti per UDP.

La funzione [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera la tabella di connessione TCP. [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) recupera la tabella del listener UDP.

La funzione [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) consente a uno sviluppatore di impostare lo stato di una connessione TCP specificata su MIB \_ TCP \_ state \_ Delete \_ TCB.

 

 




---
description: I parametri degli attributi \_ XP1 SUPPORT \_ MULTIPOINT, XP1 MULTIPOINT CONTROL PLANE e XP1 MULTIPOINT DATA PLANE nella struttura \_ \_ \_ \_ \_ \_ WSAPROTOCOL INFO di \_ Winsock.
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Attributi in WSAPROTOCOL_INFO struttura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb502c0f29f09604f80e5437774f2b481cef238aaf34f566e78886127dae1027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898551"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Attributi nella struttura INFO WSAPROTOCOL \_

A supporto della tassonomia descritta in precedenza, vengono usati tre parametri di attributo nella struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per distinguere rispettivamente gli schemi usati nei piani di controllo e di dati:

-   XP1 SUPPORT MULTIPOINT con valore 1 indica che questa voce di protocollo supporta le comunicazioni multipoint e che i \_ due parametri seguenti sono \_ significativi.
-   XP1 MULTIPOINT CONTROL PLANE indica se il piano di controllo è \_ \_ \_ rooted (valore = 1) o non rooted (valore = 0).
-   XP1 MULTIPOINT DATA PLANE indica se il piano dati è \_ \_ \_ rooted (valore = 1) o non rooted (valore = 0).

Si noti che sono presenti due voci [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) se un protocollo multipoint supportasse sia piani dati rooted che nonrooted, una voce per ognuna.

L'applicazione può usare [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) per determinare se le comunicazioni multipoint sono supportate per un determinato protocollo e, in tal caso, come è supportata rispettivamente per il controllo e i piani dati.

 

 

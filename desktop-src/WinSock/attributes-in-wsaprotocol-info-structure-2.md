---
description: XP1 \_ supportano \_ \_ \_ i parametri dell'attributo MultiPoint, XP1 Multipoint Control \_ Plan e XP1 \_ multipoint \_ data \_ plane nella struttura di informazioni WSAPROTOCOL di Winsock \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Attributi nella struttura WSAPROTOCOL_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307050"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Attributi nella struttura delle informazioni di WSAPROTOCOL \_

A supporto della tassonomia descritta in precedenza, vengono usati tre parametri di attributo nella struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per distinguere rispettivamente gli schemi usati nel controllo e nei piani dati:

-   XP1 \_ supporta \_ multipoint con un valore 1 indica che questa voce di protocollo supporta le comunicazioni multipoint e che i due parametri seguenti sono significativi.
-   \_ \_ \_ Il piano di controllo multipoint XP1 indica se il piano di controllo è radice (valore = 1) o non radice (valore = 0).
-   \_ \_ Il piano dati multipoint XP1 \_ indica se il piano dati è radice (valore = 1) o non radice (valore = 0).

Si noti che sono presenti due voci di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) se un protocollo multipoint supporta sia i piani dati radice che quelli non radice, una voce per ognuno di essi.

L'applicazione può usare [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) per individuare se le comunicazioni multipoint sono supportate per un determinato protocollo e, in tal caso, come sono supportate rispetto al controllo e ai piani dati, rispettivamente.

 

 

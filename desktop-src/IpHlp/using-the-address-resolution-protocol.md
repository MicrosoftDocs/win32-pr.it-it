---
description: È possibile usare l'helper IP per eseguire operazioni ARP (Address Resolution Protocol) per il computer locale. Usare le funzioni seguenti per recuperare e modificare la tabella ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Uso del protocollo di risoluzione degli indirizzi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca1ef7e5d657476ff85a8893d71e197a034c70234e44f32317b7b05f58c9b94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290011"
---
# <a name="using-the-address-resolution-protocol"></a>Uso del protocollo di risoluzione degli indirizzi

È possibile usare l'helper IP per eseguire operazioni ARP (Address Resolution Protocol) per il computer locale. Usare le funzioni seguenti per recuperare e modificare la tabella ARP.

[**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) recupera la tabella ARP. La tabella ARP contiene il mapping degli indirizzi IP agli indirizzi fisici. Gli indirizzi fisici vengono talvolta definiti indirizzi MAC (Media Access Controller).

Usare le [**funzioni CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) e [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) per aggiungere o rimuovere voci ARP specifiche da o verso la tabella. La [**funzione FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) elimina tutte le voci dalla tabella.

Per creare o eliminare voci ARP proxy, usare le [**funzioni CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) [**e DeleteProxyArpEntry.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)

La [**funzione SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) invia una richiesta ARP alla rete locale.

 

 




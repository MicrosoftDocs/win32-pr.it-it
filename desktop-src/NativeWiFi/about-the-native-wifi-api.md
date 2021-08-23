---
description: L'API Wi-Fi nativa contiene funzioni, strutture ed enumerazioni che supportano la connettività di rete wireless e la gestione dei profili wireless.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Informazioni sull'API Wi-Fi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fafbe65d162668930470712c79637a41fcd0ee0769441b745e68bca156ada4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685461"
---
# <a name="about-the-native-wifi-api"></a>Informazioni sull'API Wi-Fi nativa

L'API Wi-Fi nativa contiene funzioni, strutture ed enumerazioni che supportano la connettività di rete wireless e la gestione dei profili wireless. L'API può essere usata sia per l'infrastruttura che per le reti ad hoc. L'API ad hoc wireless è un'interfaccia orientata a oggetti semplificata per la creazione, la gestione e l'uso di reti ad hoc.

> [!Note]  
> La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows. A partire Windows 8.1 e Windows Server 2012 R2, [usare Wi-Fi Direct.](about-the-wi-fi-direct-api.md)

 

L'implementazione dell'API ad hoc usa l'API Wi-Fi nativa. Ciò significa che le chiamate API ad hoc possono attivare notifiche Wi-Fi native e viceversa.

Non è consigliabile combinare chiamate API Wi-Fi native e chiamate API ad hoc wireless. Gli sviluppatori devono scegliere un approccio di programmazione prima di progettare un'applicazione. Se l'applicazione usa o gestisce reti di infrastruttura, è consigliabile usare l'API Wi-Fi nativa. Se l'applicazione richiede la funzionalità di gestione del profilo, è consigliabile usare l'API Wi-Fi nativa. In caso contrario, è necessario utilizzare l'API ad hoc wireless.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Supporto dell'API Wifi nativa in Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Autorizzazioni per l'API Wi-Fi nativa](native-wifi-api-permissions.md)
</dt> <dt>

[Informazioni sull'API ad hoc wireless](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Scaricare l'SDK Windows Vista](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 




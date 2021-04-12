---
description: L'API WiFi nativa contiene funzioni, strutture ed enumerazioni che supportano la connettività di rete wireless e la gestione dei profili wireless.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Informazioni sull'API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233702"
---
# <a name="about-the-native-wifi-api"></a>Informazioni sull'API WiFi nativa

L'API WiFi nativa contiene funzioni, strutture ed enumerazioni che supportano la connettività di rete wireless e la gestione dei profili wireless. L'API può essere usata sia per le reti ad hoc che per l'infrastruttura. L'API ad hoc wireless è un'interfaccia orientata a oggetti semplificata per la creazione, la gestione e l'utilizzo di reti ad hoc.

> [!Note]  
> La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows. A partire da Windows 8.1 e Windows Server 2012 R2, usare invece [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

L'implementazione dell'API ad hoc usa l'API WiFi nativa. Ciò significa che le chiamate API ad hoc possono attivare le notifiche Wi-Fi native e viceversa.

La combinazione di chiamate API native Wi-Fi e chiamate API ad hoc wireless non è consigliata. Gli sviluppatori devono scegliere un approccio di programmazione prima di progettare un'applicazione. Se l'applicazione USA o gestisce reti di infrastruttura, è necessario usare l'API WiFi nativa. Se l'applicazione richiede funzionalità di gestione del profilo, è necessario usare l'API WiFi nativa. In caso contrario, è consigliabile usare l'API ad hoc wireless.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Supporto per le API WiFi native in Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Autorizzazioni API WiFi Native](native-wifi-api-permissions.md)
</dt> <dt>

[Informazioni sull'API ad hoc wireless](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Scarica Windows Vista SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 




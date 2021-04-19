---
description: Definisce un profilo a banda larga mobile.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Riferimento allo schema del profilo broadband mobile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307529"
---
# <a name="mobile-broadband-profile-schema-reference"></a>Riferimento allo schema del profilo broadband mobile

Lo schema del profilo Mobile Broadband definisce un profilo a banda larga mobile.

I profili archiviano i parametri di configurazione di rete e utente correlati a banda larga mobile. Vengono inoltre archiviate le preferenze dell'utente per una connessione.

L'elemento radice di un profilo Mobile Broadband è l'elemento [**MBNProfile**](schema-mbnprofile-element.md) . Ogni profilo include esattamente un elemento radice. Tutti gli elementi dello schema del profilo broadband mobile utilizzati da Windows 7 si trovano nello spazio dei nomi `https://www.microsoft.com/networking/WWAN/profile/v1` e gli elementi utilizzati da Windows 8 si trovano nello spazio dei nomi `https://www.microsoft.com/networking/WWAN/profile/v2` .

Lo schema del profilo Mobile Broadband impone rigorosamente l'ordine dei nodi. I nodi specificati in un profilo devono essere conformi allo **schema del profilo broadband mobile** e vengono visualizzati nell'ordine previsto nella definizione dello schema. Ad esempio, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) deve essere specificato immediatamente dopo [**AccessString**](schema-accessstring-contexttype-element.md).

-   [Schema profilo broadband mobile V1](mobile-broadband-profile-schema.md)
-   [Schema del profilo broadband mobile V2](mobile-broadband-profile-schema-v2.md)
-   [Schema profilo a banda larga mobile V3](mobile-broadband-profile-schema-v3.md)
-   [Schema del profilo broadband mobile V4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))

 

 

---
description: L'amministratore di sistema può impostare quote per utenti specifici in un volume. L'amministratore può anche impostare quote predefinite per il volume.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Amministrazione delle quote disco a livello di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2465d082ff93ee6a4ef02351e17e6b1214d005dc1d13be27f83db89e78c6bcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996418"
---
# <a name="system-level-administration-of-disk-quotas"></a>Amministrazione delle quote disco a livello di sistema

L'amministratore di sistema può impostare quote per utenti specifici in un volume. L'amministratore può anche impostare quote predefinite per il volume. Un nuovo utente nel volume riceve la quota predefinita, a meno che l'amministratore non stabilirà una quota specifica per tale utente.

L'amministratore può eseguire query sul livello di rilevamento e imposizione della quota (o sugli stati di quota), sui limiti di quota predefiniti e sulle informazioni sulla quota per utente. Le informazioni sulla quota per utente contengono il limite di quota rigida dell'utente, la soglia di avviso e l'utilizzo della quota. L'amministratore può anche abilitare o disabilitare l'imposizione della quota.

Esistono tre stati di quota, come illustrato nella tabella seguente.



| State          | Descrizione                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quota disabilitata | Le modifiche all'utilizzo della quota non vengono rilevate, ma i limiti di quota non vengono rimossi. In questo stato, le prestazioni non sono influenzate dalle quote del disco. Questo è lo stato predefinito.                         |
| Quota rilevata  | Le modifiche all'utilizzo della quota vengono rilevate, ma i limiti di quota non vengono applicati. In questo stato non vengono generati eventi di violazione della quota e nessuna operazione sui file ha esito negativo a causa di violazioni della quota del disco. |
| Quota applicata | Le modifiche all'utilizzo della quota vengono rilevate e vengono applicati i limiti di quota.                                                                                                                           |



 

 

 




---
description: L'amministratore di sistema può impostare le quote per utenti specifici in un volume. L'amministratore può inoltre impostare le quote predefinite per il volume.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Amministrazione a livello di sistema di quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226260"
---
# <a name="system-level-administration-of-disk-quotas"></a>Amministrazione a livello di sistema di quote disco

L'amministratore di sistema può impostare le quote per utenti specifici in un volume. L'amministratore può inoltre impostare le quote predefinite per il volume. Un nuovo utente del volume riceve la quota predefinita, a meno che l'amministratore non abbia stabilito una quota specifica per tale utente.

L'amministratore può eseguire una query sul livello di rilevamento e imposizione delle quote (o Stati delle quote), i limiti di quota predefiniti e le informazioni sulla quota per utente. Le informazioni sulla quota per utente contengono il limite di quota hardware dell'utente, la soglia di avviso e l'utilizzo della quota. L'amministratore può anche abilitare o disabilitare l'imposizione delle quote.

Sono disponibili tre stati di quota, come illustrato nella tabella seguente.



| State          | Descrizione                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quota disabilitata | Le modifiche all'utilizzo della quota non vengono rilevate, ma i limiti della quota non vengono rimossi. In questo stato le prestazioni non sono influenzate dalle quote disco. Questo è lo stato predefinito.                         |
| Quota rilevata  | Le modifiche all'utilizzo della quota vengono rilevate, ma non vengono applicati limiti di quota. In questo stato non viene generato alcun evento di violazione della quota e non vengono eseguite operazioni sui file a causa di violazioni della quota del disco. |
| Quota applicata | Vengono rilevate le modifiche all'utilizzo della quota e vengono applicati i limiti delle quote.                                                                                                                           |



 

 

 




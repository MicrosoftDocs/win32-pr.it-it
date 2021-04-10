---
description: Il sottosistema POSIX deve essere in grado di convertire qualsiasi ID di sicurezza (SID) rilevato in un valore a 32 bit, detto ID POSIX.
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: Mapping degli identificatori POSIX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabb944b543fba65942eb89d526590a5aff2c26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884278"
---
# <a name="mapping-posix-identifiers"></a>Mapping degli identificatori POSIX

Il sottosistema POSIX deve essere in grado di convertire qualsiasi ID di [*sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) rilevato in un valore a 32 bit, detto *ID POSIX*. Inoltre, deve essere in grado di classificare l'ID come ID utente o ID gruppo. Per comprendere il modo in cui viene eseguito questo mapping, esaminiamo prima i SID di cui è necessario eseguire il mapping.

I SID hanno due componenti, il SID del dominio e l'ID relativo dell'account nel dominio. Ad esempio, nel SID S-1-518364-21-43-8, l'ultimo numero, 8, è l'ID relativo (RID) dell'account e S-1-518364-21-43 è il SID del dominio.

Le informazioni sul dominio sono archiviate in oggetti [**trustedDomain**](trusteddomain-object.md) . Una parte delle informazioni archiviate in un oggetto **trustedDomain** è un offset ID POSIX da usare per i SID in tale dominio. Si supponga, ad esempio, che un **trustedDomain** venga definito come segue:

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

Gli ID POSIX per gli account in questo dominio verranno generati aggiungendo 0x130000 all'ID relativo dell'account. Quindi, l'ID POSIX corrispondente al SID S-1-518364-21-43-8 sarebbe 0x130008.

Non tutte le traduzioni con ID POSIX usano un oggetto [**trustedDomain**](trusteddomain-object.md) . La tabella seguente illustra i SID di cui è stato eseguito il mapping con valori di offset noti.



| Source (Sorgente)                                              | Offset ID POSIX |
|-----------------------------------------------------|-----------------|
| SID dal dominio predefinito                       | 0x20000         |
| SID del dominio dell'account                        | 0x30000         |
| SID del dominio primario (solo per workstation) | 0x40000         |



 

Infine, un altro set di SID, SID di accesso, richiede un'elaborazione speciale. Questi valori vengono assegnati dal processo di accesso di Windows per ogni sessione di accesso e hanno il formato S-1-5-5-X-Y, dove X e Y vengono considerati come un singolo \_ numero intero grande incrementato per ogni sessione di accesso. Questi SID vengono mappati alla costante ID POSIX 0xFFF. Per eseguire il mapping dell'ID POSIX 0xFFF, è possibile convertire qualsiasi [*identificatore di accesso*](/windows/desktop/SecGloss/l-gly) più adatto alla situazione oppure è possibile usare S-1-5-5-0-0 per impostazione predefinita. Se, ad esempio, un utente POSIX applica la protezione a un oggetto e specifica FFFx, è preferibile sostituire l'identificatore di accesso dell'utente piuttosto che assegnare solo S-1-5-5-0-0.

 

 

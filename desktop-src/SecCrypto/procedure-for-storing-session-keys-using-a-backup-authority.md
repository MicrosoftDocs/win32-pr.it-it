---
description: Un'applicazione che usa un'autorità di backup per archiviare le chiavi di sessione in genere segue questi passaggi.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Archiviazione delle chiavi di sessione tramite un'autorità di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbd8d8fd4bebeb4b5f3c3711f4e64b9c023f57404e8d9f93200e00967dfbed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977455"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Archiviazione delle chiavi di sessione tramite un'autorità di backup

Un'applicazione che usa [*un'autorità di backup*](../secgloss/b-gly.md) per archiviare le chiavi di sessione in genere segue questi passaggi.

**Per usare un'autorità di backup**

1.  Crittografare il file come di consueto.
2.  Esportare [*la chiave di*](../secgloss/s-gly.md) sessione usata per crittografare il file in un [*BLOB*](../secgloss/s-gly.md)di chiave semplice, specificando che per crittografare il BLOB della chiave deve essere usata la chiave pubblica dello [*scambio*](../secgloss/k-gly.md) di chiavi. Archiviare questo BLOB della chiave con il file crittografato.
3.  Esportare nuovamente la chiave di sessione, questa volta specificando che la chiave pubblica dell'autorità di backup deve essere usata per crittografare il BLOB della chiave. Inviare questo BLOB della chiave all'autorità di backup, insieme alla descrizione della chiave, al numero di serie e così via.

Se una [*coppia di chiavi*](../secgloss/k-gly.md) viene persa, le chiavi possono essere recuperate dall'autorità di [*backup*](../secgloss/b-gly.md) se è possibile stabilire l'identità del proprietario delle chiavi. La procedura per stabilire l'identità è determinata dai criteri dell'autorità di backup specifica e non comporta CryptoAPI.

Per il codice necessario per creare una chiave di sessione ed esportarne una in un [*BLOB*](../secgloss/s-gly.md) di chiave semplice che può essere scritto in un file su disco, vedere Esempio [di programma C: Esportazione](example-c-program-exporting-a-session-key.md)di una chiave di sessione .

 

 

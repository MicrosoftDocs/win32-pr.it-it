---
description: Un'applicazione che utilizza un'autorità di backup per archiviare le chiavi di sessione in genere segue questa procedura.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Archiviazione di chiavi di sessione mediante un'autorità di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345726"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Archiviazione di chiavi di sessione mediante un'autorità di backup

Un'applicazione che utilizza un' [*autorità di backup*](../secgloss/b-gly.md) per archiviare le chiavi di sessione in genere segue questa procedura.

**Per utilizzare un'autorità di backup**

1.  Crittografare il file come di consueto.
2.  Esportare la [*chiave di sessione*](../secgloss/s-gly.md) usata per crittografare il file in un [*BLOB di chiavi semplice*](../secgloss/s-gly.md), specificando che la chiave [*pubblica di scambio*](../secgloss/k-gly.md) della chiave deve essere usata per crittografare il BLOB della chiave. Archiviare questo BLOB di chiavi con il file crittografato.
3.  Esportare di nuovo la chiave di sessione, questa volta specificando che la chiave pubblica dell'autorità di backup verrà usata per crittografare il BLOB della chiave. Inviare questo BLOB di chiavi all'autorità di backup, insieme alla descrizione della chiave, al numero di serie e così via.

Se una [*coppia di chiavi*](../secgloss/k-gly.md) viene persa, le chiavi possono essere recuperate dall' [*autorità di backup*](../secgloss/b-gly.md) se è possibile stabilire l'identità del proprietario delle chiavi. La procedura per stabilire l'identità è determinata dai criteri dell'autorità di backup specifica e non comporta CryptoAPI.

Per il codice necessario per creare una chiave della sessione ed esportare la chiave in un [*BLOB di chiavi semplice*](../secgloss/s-gly.md) che può essere scritto in un file su disco, vedere [esempio C Program: exporting a Session Key](example-c-program-exporting-a-session-key.md).

 

 

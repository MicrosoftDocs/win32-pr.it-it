---
description: Se l'azione InstallValidate rileva l'installazione di un file in uso, viene visualizzata la finestra di dialogo filesinus e vengono registrate le informazioni seguenti.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Registrazione delle richieste di riavvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530234"
---
# <a name="logging-of-reboot-requests"></a>Registrazione delle richieste di riavvio

Se l' [azione InstallValidate](installvalidate-action.md) rileva l'installazione di un file in uso, viene visualizzata la [finestra di dialogo filesinus](filesinuse-dialog.md) e vengono registrate le informazioni seguenti.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

Se il programma di installazione rileva che sta per sovrascrivere un file in uso, registra le informazioni seguenti.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

Il \[ token del nome file \] può effettivamente contenere un percorso di un file con estensione RBF. In questo caso il file con estensione RBF è effettivamente il file originale registrato dal messaggio 1603 che è stato rinominato nel file. RBF. Il file in uso viene innanzitutto rinominato con estensione RBF, quindi viene eliminato.

Per ottenere ulteriori informazioni sui motivi per cui il programma di installazione tenta di sovrascrivere il file specifico, è possibile utilizzare l'opzione di registrazione dettagliata. Usare il \_ valore dettagliato INSTALLLOGMODE in una chiamata a [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o usare l'opzione output dettagliato delle opzioni della [riga di comando](command-line-options.md). Vengono registrate le informazioni seguenti.

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

Il log includerà un messaggio come "il file esistente è una versione più bassa" o "file esistente danneggiato (checksum non valido)"

 

 




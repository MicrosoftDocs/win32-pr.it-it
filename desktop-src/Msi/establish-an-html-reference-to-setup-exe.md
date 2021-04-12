---
description: Il passaggio finale consiste nell'inserire un riferimento al Setup.exe nella pagina Web ipotetica di configurazione (MySetup.html) descritta in un esempio di installazione Windows Installer basato su URL.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Definire un riferimento HTML a Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231873"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Definire un riferimento HTML a Setup.exe

Il passaggio finale consiste nell'inserire un riferimento al Setup.exe nella pagina Web ipotetica di configurazione (MySetup.html) descritta in [un esempio di installazione Windows Installer basato su URL](a-url-based-windows-installer-installation-example.md). Usare lo script HTML seguente:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Facendo clic sul collegamento "installazione di configurazione" si presenta agli utenti l'opzione per salvare o eseguire da tale percorso. Se l'utente seleziona Esegui da tale posizione, il Setup.exe aggiorna la versione di Windows Installer nel computer, se necessario, verifica la firma digitale nel pacchetto di installazione e installa il pacchetto nel computer.

Questa operazione completa l'esempio.

 

 




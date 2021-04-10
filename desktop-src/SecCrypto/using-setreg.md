---
description: Lo strumento SetReg imposta il valore delle chiavi del registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Uso di SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130238"
---
# <a name="using-setreg"></a>Uso di SetReg

Lo strumento SetReg imposta il valore delle chiavi del registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode. Queste chiavi, denominate chiavi di stato di pubblicazione software, controllano se considerare attendibile una radice di test, consentire l'approvazione offline dei certificati, verificare le date di scadenza del certificato ed eseguire controlli di revoca.

Il comando seguente elenca la sintassi e le opzioni per l'uso di SetReg.

**setreg-?**

Il seguente comando rende attendibile la radice del test. Per impostazione predefinita, una radice di test non è attendibile. Dopo aver apportato le modifiche ai valori di chiave, viene visualizzato un elenco del valore corrente di tutti i valori di chiave. Se si usa l'opzione **-q** , i valori di chiave non vengono visualizzati.

**setreg 1 TRUE**

Il seguente comando rende una radice di test non attendibile e determina la revoca di tutti i controlli. L'opzione **-q** viene usata in modo che l'elenco di valori di chiave non venga visualizzato

**setreg-q 1 FALSE 3 TRUE**

> [!Note]  
> I comandi, le opzioni e gli argomenti non fanno distinzione tra maiuscole e minuscole.

 

 

 




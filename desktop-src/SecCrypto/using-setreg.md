---
description: Lo strumento SetReg imposta il valore delle chiavi del Registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Uso di SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0de37d236b978217d8c2a713e9595fbaad70afb69beb32cd0f5200738d2d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896738"
---
# <a name="using-setreg"></a>Uso di SetReg

Lo strumento SetReg imposta il valore delle chiavi del Registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode. Queste chiavi, denominate chiavi di stato di pubblicazione software, controllano se considerare attendibile una radice di test, consentire l'approvazione offline dei certificati, testare le date di scadenza dei certificati ed eseguire controlli di revoca.

Il comando seguente elenca la sintassi e le opzioni per l'uso di SetReg.

**setreg -?**

Il comando seguente rende attendibile una radice di test. Per impostazione predefinita, una radice di test non è attendibile. Dopo aver apportato modifiche ai valori di chiave, viene visualizzato un elenco del valore corrente di tutti i valori chiave. Se si **usa l'opzione -q,** i valori della chiave non vengono visualizzati.

**setreg 1 TRUE**

Il comando seguente rende una radice di test non attendibile e fa in modo che tutte le verifiche controllino la revoca. **L'opzione -q** viene usata in modo che l'elenco di valori di chiave non sia visualizzato

**setreg -q 1 FALSE 3 TRUE**

> [!Note]  
> Per comandi, opzioni e argomenti non viene fatto distinzione tra maiuscole e minuscole.

 

 

 




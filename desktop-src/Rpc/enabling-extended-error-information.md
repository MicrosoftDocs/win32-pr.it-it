---
title: Abilitazione di informazioni estese sugli errori
description: Abilitazione di informazioni estese sugli errori per RPC (Remote Procedure Call).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221688"
---
# <a name="enabling-extended-error-information"></a>Abilitazione di informazioni estese sugli errori

Per abilitare le informazioni estese sugli errori, seguire questa procedura:

Aprire i criteri del computer locale usando l'interfaccia gpedit. msc.

Passare al criterio individuato in configurazione computer/Modelli amministrativi/sistema/chiamata procedura remota/supporto per la risoluzione dei problemi RPC/propagazione delle informazioni sugli errori estesi

Abilitare i criteri e impostare la **propagazione dei campi delle informazioni sugli errori estesi** su "on".

Questo processo converte la propagazione delle informazioni di errore estese in per tutti i processi nel computer.

Per abilitare le informazioni estese sugli errori solo per determinati processi in un computer o per disabilitarlo solo per determinati processi nel computer, utilizzare le opzioni **disattivata con eccezioni** o **con eccezioni** . Entrambe le opzioni utilizzano le **eccezioni delle informazioni sugli errori estesi** del campo per specificare i processi che hanno l'impostazione predefinita e i processi che hanno il contrario rispetto all'impostazione predefinita. **Le eccezioni delle informazioni sugli errori estesi** contengono un elenco di nomi di processo.

Se la riga di comando di un processo inizia con una stringa che si trova nelle **eccezioni delle informazioni di errore estese**, il processo riceverà il contrario rispetto all'impostazione predefinita. Se, ad esempio, si desidera che tutti i processi nel computer propaghino informazioni estese sugli errori, ad eccezione di LSASS e del processo denominato **server protetto**, impostare la **propagazione delle informazioni sugli errori estesi** su **on con le eccezioni** e specificare nel campo eccezioni per le **informazioni sugli errori** estesi la stringa seguente: lsass "server protetto".

Le stringhe possono essere racchiuse tra virgolette doppie, ma questa operazione è facoltativa se non sono presenti spazi nella stringa. Inoltre, è possibile specificare l'inizio della riga di comando del processo. Se, ad esempio, si specifica **off con le eccezioni** nella **propagazione del campo informazioni sugli errori estesi** e nel campo eccezioni per le **informazioni sugli errori estesi** , viene specificato quanto segue: Win.

Ogni processo che inizia con "Win" propaga le informazioni estese sull'errore. In molti computer, ad esempio, questi processi sarebbero winlogon.exe e WINWORD.EXE.

 

 





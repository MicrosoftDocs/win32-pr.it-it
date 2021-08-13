---
title: Errori comuni (ADSI)
description: Tutti gli errori specifici di ADSI hanno una forma esadecimale di 80005xxx. I codici di errore più comuni rilevati sono descritti nella tabella seguente.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efcbbbce67d9928c9ecda3840f34a1cbf6faae79ca4d9fe72830a5b57881177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692195"
---
# <a name="common-errors-adsi"></a>Errori comuni (ADSI)

Tutti gli errori specifici di ADSI hanno una forma esadecimale di 80005xxx. I codici di errore più comuni rilevati sono descritti nella tabella seguente.



| Codice errore esadecimale ADSI | Descrizione                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | È stato passato un nome di percorso ADSI non valido. Questo errore è il risultato del passaggio di ADsPath non corretto a **GetObject durante** l'associazione a un oggetto.<br/> |
| 8000500D<br/> | Impossibile trovare la proprietà ADSI nella cache delle proprietà.<br/>                                                                                 |
| 8000500E<br/> | L'oggetto ADSI esiste. Se si tenta di creare un oggetto ADSI con lo stesso nome di un oggetto ADSI esistente, si verificherà questo errore.<br/>    |



 

Per un elenco completo dei codici di errore ADSI, vedere [Codici di errore ADSI generici.](generic-adsi-error-codes.md)

## <a name="com-errors"></a>Errori COM

Poiché ADSI è costituito da oggetti COM, restituirà codici di errore COM standard. Nella tabella seguente sono elencati i codici di errore COM più comunemente rilevati nella programmazione ADSI.



| Codice di errore esadecimale COM  | Descrizione                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Errore non specificato. La causa dell'errore dell'oggetto COM è indeterminata da ADSI. <br/>                                  |
| 800041E4<br/> | Oggetto non trovato. Questo errore si verifica principalmente a causa di un errore di ortografia nella stringa ADsPath durante l'associazione a un oggetto.<br/> |



 

Per [altri esempi di](generic-com-error-codes.md) errori COM che possono verificarsi nella programmazione ADSI, vedere Codici di errore COM generici.

## <a name="win32-errors"></a>Errori Win32

Qualsiasi codice di errore nel formato esadecimale 8007xxxx è un codice di errore Win32 standard. Se si convertono le ultime quattro cifre da esadecimale a decimale, è possibile accedere all'errore dalla riga di comando Windows 2000:

**net helpmsg <number>**

Nella riga di comando precedente " number " è il numero decimale ottenuto convertendo le ultime quattro cifre del codice di &lt; &gt; errore da esadecimale. Questa riga di comando fornirà una descrizione più utile dell'errore Win32, che può essere di grande aiuto per il debug dello script.

 

 






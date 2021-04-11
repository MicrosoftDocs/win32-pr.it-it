---
title: Errori comuni (ADSI)
description: Tutti gli errori specifici di ADSI hanno un formato esadecimale di 80005xxx. I codici di errore più comuni rilevati sono descritti nella tabella seguente.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "104335988"
---
# <a name="common-errors-adsi"></a>Errori comuni (ADSI)

Tutti gli errori specifici di ADSI hanno un formato esadecimale di 80005xxx. I codici di errore più comuni rilevati sono descritti nella tabella seguente.



| Codice errore esadecimale ADSI | Descrizione                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | È stato passato un percorso ADSI non valido. Questo errore deriva dal passaggio di un ADsPath in formato non corretto a **GetObject** durante l'associazione a un oggetto.<br/> |
| 8000500D<br/> | La proprietà ADSI non è stata trovata nella cache delle proprietà.<br/>                                                                                 |
| 8000500E<br/> | L'oggetto ADSI esiste. Questo errore si verificherà se si tenta di creare un oggetto ADSI con lo stesso nome di un oggetto ADSI esistente.<br/>    |



 

Per un elenco completo dei codici di errore ADSI, vedere [codici di errore ADSI generici](generic-adsi-error-codes.md).

## <a name="com-errors"></a>Errori COM

Poiché ADSI è costituito da oggetti COM, restituirà codici di errore COM standard. Nella tabella seguente sono elencati i codici di errore COM più comunemente rilevati nella programmazione ADSI.



| Codice errore esadecimale COM  | Descrizione                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Errore non specificato. La cause dell'errore dell'oggetto COM è indeterminata da ADSI. <br/>                                  |
| 800041E4<br/> | Oggetto non trovato. Questo errore si verifica principalmente a causa dell'errore di ortografia della stringa ADsPath durante l'associazione a un oggetto.<br/> |



 

Vedere [codici di errore com generici](generic-com-error-codes.md) per altri esempi di errori com che possono verificarsi nella programmazione ADSI.

## <a name="win32-errors"></a>Errori Win32

Qualsiasi codice di errore del formato esadecimale 8007xxxx è un codice di errore Win32 standard. Se si convertono le ultime quattro cifre da esadecimali a decimali, è possibile accedere all'errore dalla riga di comando di Windows 2000:

**helpmsg NET <number>**

Nella riga di comando precedente, " &lt; Number &gt; " è il numero decimale ottenuto convertendo le ultime quattro cifre del codice di errore da esadecimale. Questa riga di comando fornirà una descrizione più utile dell'errore Win32, che può essere molto utile per il debug dello script.

 

 






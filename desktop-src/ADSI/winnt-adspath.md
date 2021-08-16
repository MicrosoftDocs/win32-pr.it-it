---
title: WinNT ADsPath
description: Questo argomento contiene esempi di stringhe da usare per WinNT ADsPath.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Provider di servizi WinNT ADSI , WinNT ADsPath
- ADsPath ADSI , WinNT, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4971209a516d9e0c759e892322c99db1807a4bf88e771281299af30abc47d47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838371"
---
# <a name="winnt-adspath"></a>WinNT ADsPath

La stringa ADsPath per il provider ADSI WinNT può avere uno dei formati seguenti:


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



Il nome di dominio può essere un nome NETBIOS o un nome DNS.

Il server è il nome di un server specifico all'interno del dominio.

Il percorso è il percorso dell'oggetto , ad esempio "printserver1/printer2".

Il nome dell'oggetto è il nome di un oggetto specifico.

La classe dell'oggetto è il nome della classe dell'oggetto denominato. Un esempio di questo utilizzo è "WinNT://MyServer/JeffSmith,user". La specifica di un nome di classe può migliorare le prestazioni dell'operazione di associazione.

 

 





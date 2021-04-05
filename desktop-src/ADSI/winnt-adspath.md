---
title: ADsPath WinNT
description: Questo argomento contiene esempi di stringhe da usare per la ADsPath WinNT.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Provider di servizi WinNT ADSI, WinNT ADsPath
- ADsPath ADSI, WinNT, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955072"
---
# <a name="winnt-adspath"></a>ADsPath WinNT

La stringa ADsPath per il provider ADSI WinNT può essere una delle seguenti forme:


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

Il percorso è il percorso dell'oggetto, ad esempio "printserver1/Printer2".

Il nome dell'oggetto è il nome di un oggetto specifico.

La classe Object è il nome della classe dell'oggetto denominato. Un esempio di questo utilizzo è "WinNT://MyServer/JeffSmith,user". La specifica di un nome di classe può migliorare le prestazioni dell'operazione di associazione.

 

 





---
title: Spazi dei nomi
description: Gli oggetti che risiedono all'interno di un determinato spazio dei nomi sono identificati da un nome univoco.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- spazi dei nomi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395282"
---
# <a name="namespaces"></a>Spazi dei nomi

Gli oggetti che risiedono all'interno di un determinato spazio dei nomi sono identificati da un nome univoco. Ad esempio, i file archiviati in un'unità disco del PC si trovano nello spazio dei nomi file system. Il nome univoco di un file è basato sulla posizione in cui è archiviato nello spazio dei nomi file system. Ad esempio:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Gli spazi dei nomi del servizio directory identificano inoltre gli oggetti in essi contenuti in base a nomi univoci, che in genere sono basati sul percorso nella directory in cui è possibile trovare l'oggetto. Ad esempio, in una directory X. 500, un oggetto specificato potrebbe avere un nome simile al seguente:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Servizi directory diversi utilizzano moduli diversi per la denominazione degli oggetti in essi contenuti. In questo modo è possibile affrontare diversi spazi dei nomi, in particolare per gli sviluppatori, considerando tutti i diversi ambienti in cui il codice potrebbe essere in esecuzione.

Uno degli obiettivi di Active Directory Service Interfaces (ADSI) consiste nel fornire un Framework di denominazione che consenta l'accesso agli spazi dei nomi dei diversi provider di servizi di directory.

ADSI definisce una convenzione di denominazione che può identificare in modo univoco un oggetto in un ambiente eterogeneo. Questi nomi sono denominati stringhe ADsPath. Le stringhe ADsPath accettano diverse forme:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



È possibile introdurre formati ADsPath aggiuntivi da provider ADSI diversi, ad esempio il provider ADSI per il server Internet Information Services, che supportano "IIS://" ADsPaths).

 

 





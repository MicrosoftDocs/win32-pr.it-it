---
title: Spazi dei nomi
description: Gli oggetti che risiedono all'interno di uno spazio dei nomi specificato sono identificati da un nome univoco.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- spazi dei nomi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d416782f2a96ca716f6e803ad9d0b4200c82cff6ad0ad033751a89a5d2c8af1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839383"
---
# <a name="namespaces"></a>Spazi dei nomi

Gli oggetti che risiedono all'interno di uno spazio dei nomi specificato sono identificati da un nome univoco. Ad esempio, i file archiviati in un'unità disco del PC si trovano nello spazio file system spazio dei nomi . Il nome univoco di un file si basa sulla posizione in cui è archiviato nello spazio dei nomi file system dati. Esempio:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Gli spazi dei nomi del servizio directory identificano anche gli oggetti che contengono in base a nomi univoci che in genere si basano sul percorso nella directory in cui è possibile trovare l'oggetto. Ad esempio, in una directory X.500 un determinato oggetto potrebbe avere un nome simile al seguente:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Servizi directory diversi usano forme diverse per assegnare un nome agli oggetti in essi contenuti. Ciò rende difficile gestire spazi dei nomi diversi, in particolare per gli sviluppatori, considerando tutti i diversi ambienti in cui il codice potrebbe essere in esecuzione.

L'obiettivo di Active Directory Service Interfaces (ADSI) è fornire un framework di denominazione che consenta l'accesso a spazi dei nomi di provider di servizi directory diversi.

ADSI definisce una convenzione di denominazione in grado di identificare in modo univoco un oggetto in un ambiente eterogeneo. Questi nomi sono denominati stringhe ADsPath. Le stringhe ADsPath hanno diverse forme:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



Altri formati ADsPath possono essere introdotti da diversi provider ADSI, ad esempio il provider ADSI per il server Internet Information Services, che supportano gli ADsPath "IIS://".

 

 





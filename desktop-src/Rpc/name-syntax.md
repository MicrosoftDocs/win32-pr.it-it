---
title: Sintassi dei nomi
description: Rpc (Remote Procedure Call) e sintassi del nome.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f63c86e6fe9283855e886014787fe36361bfbcdea3bc53e4078bbb43d193293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927820"
---
# <a name="name-syntax"></a>Sintassi dei nomi

Microsoft RPC accetta nomi conformi alla sintassi seguente:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Specifica un identificatore che può contenere qualsiasi carattere ad eccezione del carattere barra (/).

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>Domainname
</dt> <dd>

Specifica il nome del dominio.

</dd> </dl>

Un parametro che seleziona il tipo di sintassi del nome e la stringa che specifica il nome vengono forniti a molte delle funzioni RPC NSI (Name Service Interface).

Microsoft RPC supporta un solo tipo di sintassi dei nomi, come specificato dalla costante RPC \_ \_ CS \_ SYNTAX \_ DCE. Questa costante è definita nel file di intestazione RPCNSI.H.

La sintassi del nome specificata da RPC C NS SYNTAX DCE è un'estensione della sintassi dei nomi \_ \_ \_ \_ \_ DCE Cell Directory Service (CDS) di OSF. La possibilità di specificare un nome di dominio rappresenta un'estensione di tale sintassi. Non esiste alcun limite assoluto al numero di nomi che possono essere separati da barre purché la stringa complessiva sia inferiore a 256 caratteri.

Le barre consentono di specificare una struttura logica per il nome, ma non corrispondono a una struttura logica negli oggetti stessi.

 

 





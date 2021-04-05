---
title: Sintassi del nome
description: RPC (Remote Procedure Call) e sintassi del nome.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955653"
---
# <a name="name-syntax"></a>Sintassi del nome

Microsoft RPC accetta nomi conformi alla sintassi seguente:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="name"></span><span id="NAME"></span>nome
</dt> <dd>

Specifica un identificatore che può contenere qualsiasi carattere eccetto il carattere barra (/) di delimitazione.

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>NomeDominio
</dt> <dd>

Specifica il nome del dominio.

</dd> </dl>

Un parametro che seleziona il tipo di sintassi del nome e la stringa che specifica il nome vengono forniti a molte delle funzioni RPC NSI (Name Service Interface).

Microsoft RPC supporta solo un tipo di sintassi dei nomi, come specificato dalla costante RPC \_ C \_ NS \_ sintassi \_ DCE. Questa costante viene definita nel file di intestazione RPCNSI. H.

La sintassi del nome specificata dalla sintassi RPC \_ C \_ NS \_ \_ (DCE) è un'estensione della \_ sintassi del nome del servizio di directory di celle (CDS) OSF DCE. La possibilità di specificare un nome di dominio rappresenta un'estensione di tale sintassi. Non esiste alcun limite assoluto per il numero di nomi che possono essere separati da una barra, purché la stringa complessiva sia inferiore a 256 caratteri.

Le barre consentono di specificare una struttura logica per il nome, ma non corrispondono a una struttura logica negli oggetti stessi.

 

 





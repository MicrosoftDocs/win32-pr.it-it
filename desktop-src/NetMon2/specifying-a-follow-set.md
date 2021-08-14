---
description: Un set di seguire specifica i protocolli che seguono un protocollo. Network Monitor usa un set di follow quando il parser non è in grado di identificare il protocollo successivo dai dati in un'istanza del protocollo.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Specifica di un set di follow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b11320872cc07d69f5796e344a1d5ed4dea4594e48f9697901126d915fd7b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363047"
---
# <a name="specifying-a-follow-set"></a>Specifica di un set di follow

Un set di seguire specifica i protocolli che seguono un protocollo. Network Monitor usa un set di follow quando il parser non è in grado di identificare il protocollo successivo dai dati in un'istanza del protocollo.

Ad esempio, il parser NetBIOS specifica un set di follow perché i dati nel protocollo NetBIOS non identificano il protocollo successivo. Di conseguenza, il parser NetBIOS deve creare un set di tutti i protocolli che possono seguire.

L'esempio di codice seguente identifica il set di follow netBIOS nel file [*Parser.ini.*](p.md) Il set seguente contiene i protocolli SMB (Server Message Block) e MSRPC (Microsoft Remote Procedure Call). Questi sono gli unici protocolli che possono seguire un'istanza del protocollo NetBIOS.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Un parser specifica un set di follow durante l'implementazione della [**funzione ParserAutoInstallInfo.**](parserautoinstallinfo.md) Un parser può specificare quali protocolli precedono e quali protocolli seguono. Quando un parser specifica i protocolli che precedono, Network Monitor il protocollo del parser ai set seguenti dei protocolli specificati. Quando un parser specifica i protocolli seguenti, Network Monitor crea una nuova sezione nel file Parser.ini che include il set seguente del parser.

 

 




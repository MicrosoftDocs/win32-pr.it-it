---
description: Un set di seguito specifica i protocolli che seguono un protocollo. Network Monitor utilizza un set di seguito quando il parser non è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Specifica di un set di seguito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307821"
---
# <a name="specifying-a-follow-set"></a>Specifica di un set di seguito

Un set di seguito specifica i protocolli che seguono un protocollo. Network Monitor utilizza un set di seguito quando il parser non è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.

Il parser NetBIOS, ad esempio, specifica un set di seguito poiché i dati nel protocollo NetBIOS non identificano il protocollo successivo. Di conseguenza, il parser NetBIOS deve creare un set di tutti i protocolli che può seguire.

Nell'esempio di codice seguente viene identificato il set NetBIOS follow nel file di [*Parser.ini*](p.md) . Il set seguente contiene i protocolli Server Message Block (SMB) e Microsoft Remote Procedure Call (MSRPC). Questi sono gli unici protocolli che possono seguire un'istanza del protocollo NetBIOS.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Un parser specifica un set di seguito durante l'implementazione della funzione [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . Un parser può specificare quali protocolli precedono e quali protocolli seguono. Quando un parser specifica i protocolli precedenti, Network Monitor aggiunge il protocollo del parser ai set seguenti dei protocolli specificati. Quando un parser specifica i protocolli che seguono, Network Monitor crea una nuova sezione nel file Parser.ini che include il set di seguito del parser.

 

 




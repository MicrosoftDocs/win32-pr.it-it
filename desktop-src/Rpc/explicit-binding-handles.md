---
title: Handle di binding espliciti
description: Per il massimo controllo sul processo di associazione, le applicazioni client/server possono utilizzare handle di binding espliciti.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298343"
---
# <a name="explicit-binding-handles"></a>Handle di binding espliciti

Per il massimo controllo sul processo di associazione, le applicazioni client/server possono utilizzare handle di binding espliciti. Analogamente agli handle impliciti, gli handle di binding espliciti consentono all'applicazione client di selezionare un server per l'esecuzione delle chiamate. Inoltre, gli handle di binding espliciti consentono all'applicazione client/server di creare una sessione di comunicazione RPC autenticata. Con gli handle espliciti, il client può connettersi a più di un server ed eseguire procedure remote su più server. Le applicazioni client multithreading e asincrone possono anche connettersi a più server ed eseguire contemporaneamente più procedure remote.

L'applicazione client deve passare l'handle esplicito come parametro a ogni chiamata di procedura remota. Per essere conforme allo standard OSF, l'handle deve essere specificato come primo parametro in ogni procedura remota. Tuttavia, le estensioni Microsoft per RPC consentono di specificare il gestore di associazione in altre posizioni. Per ulteriori informazioni, vedere [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).

Per creare un handle esplicito, dichiarare l'handle come parametro per le operazioni remote nel file IDL. È possibile ridefinire l' [esempio Hello World](tutorial.md) per usare un handle esplicito, come illustrato di seguito:

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

È possibile combinare handle espliciti e impliciti in una singola interfaccia. Se una funzione dispone di un handle esplicito nell'elenco di parametri, verrà usato tale handle. Se una funzione in un'interfaccia che usa handle impliciti non specifica un handle esplicito, verrà utilizzato l'handle implicito predefinito.

 

 





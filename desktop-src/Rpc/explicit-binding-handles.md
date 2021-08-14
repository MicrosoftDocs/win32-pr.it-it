---
title: Handle di associazione espliciti
description: Per il massimo controllo sul processo di associazione, le applicazioni client/server possono usare handle di associazione espliciti.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a6e723d8559dc5e72783412eb6250f69431f31d08a92c4984fb2e2a19b761d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930020"
---
# <a name="explicit-binding-handles"></a>Handle di associazione espliciti

Per il massimo controllo sul processo di associazione, le applicazioni client/server possono usare handle di associazione espliciti. Analogamente agli handle impliciti, gli handle di associazione espliciti consentono all'applicazione client di selezionare un server per eseguire le chiamate. Inoltre, gli handle di associazione espliciti consentono all'applicazione client/server di creare una sessione di comunicazione RPC autenticata. Con handle espliciti, il client può connettersi a più di un server ed eseguire procedure remote su più server. Le applicazioni client multithreading e asincrone possono anche connettersi a più server ed eseguire più procedure remote contemporaneamente.

L'applicazione client deve passare l'handle esplicito come parametro a ogni chiamata di procedura remota. Per essere conforme allo standard OSF, l'handle deve essere specificato come primo parametro in ogni procedura remota. Tuttavia, le estensioni Microsoft per RPC consentono di specificare l'handle di associazione in altre posizioni. Per altre informazioni, vedere [Microsoft RPC Binding-Handle Extensions.](microsoft-rpc-binding-handle-extensions.md)

Per creare un handle esplicito, dichiarare l'handle come parametro per le operazioni remote nel file IDL. [L'esempio Hello, World](tutorial.md) può essere ridefinito per usare un handle esplicito, come illustrato di seguito:

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

È possibile combinare handle espliciti e impliciti in una singola interfaccia. Se una funzione ha un handle esplicito nel relativo elenco di parametri, verrà usato tale handle. Se una funzione in un'interfaccia che usa handle impliciti non specifica un handle esplicito, verrà usato l'handle implicito predefinito.

 

 





---
title: Il file ACF
description: Il file ACF consente di personalizzare l'interfaccia RPC del client e/o delle applicazioni server senza influire sulle caratteristiche di rete dell'interfaccia.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963412"
---
# <a name="the-acf-file"></a>Il file ACF

Il file ACF consente di personalizzare l'interfaccia RPC del client e/o delle applicazioni server senza influire sulle caratteristiche di rete dell'interfaccia. Se, ad esempio, l'applicazione client contiene una struttura di dati complessa che ha un significato solo nel computer locale, è possibile specificare nel file ACF il modo in cui i dati della struttura possono essere rappresentati in un form indipendente dal computer per le chiamate di procedure remote.

In questa esercitazione viene illustrato un altro utilizzo del file ACF, che specifica il tipo di handle di associazione che rappresenta la connessione tra client e server. L' **\[** [**attributo \_ handle implicito**](/windows/desktop/Midl/implicit-handle) **\]** nell'intestazione ACF consente all'applicazione client di selezionare un server per la chiamata di procedura remota. L'oggetto ACF definisce l'handle che deve essere del tipo [**handle \_ t**](/windows/desktop/Midl/handle-t) (un tipo di dati primitivo MIDL). Il compilatore MIDL inserisce il nome dell'handle di associazione specificato da ACF, Hello \_ IfHandle nel file di intestazione generato. Si noti che questo particolare file ACF ha un corpo vuoto.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

Il compilatore MIDL dispone di un'opzione, [**/app \_ config**](/windows/desktop/Midl/-app-config), che consente di includere determinati attributi ACF, ad **esempio \_ handle implicito**, nel file IDL, anziché creare un file ACF separato. Provare a usare questa opzione se l'applicazione non richiede una grande configurazione speciale e se la compatibilità OSF rigida non costituisce un problema.

 

 
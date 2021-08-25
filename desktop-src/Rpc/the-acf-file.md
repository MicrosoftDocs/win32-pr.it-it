---
title: The ACF File
description: Il file ACF consente di personalizzare l'interfaccia RPC delle applicazioni client e/o server senza influire sulle caratteristiche di rete dell'interfaccia.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d234b30c25870dd7a21cb790cc4839236ab69093291285b64c870cf7c05cb11f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080841"
---
# <a name="the-acf-file"></a>The ACF File

Il file ACF consente di personalizzare l'interfaccia RPC delle applicazioni client e/o server senza influire sulle caratteristiche di rete dell'interfaccia. Ad esempio, se l'applicazione client contiene una struttura di dati complessa che ha significato solo nel computer locale, è possibile specificare nel file ACF come i dati in tale struttura possono essere rappresentati in un modulo indipendente dal computer per le chiamate di procedura remota.

Questa esercitazione illustra un altro uso del file ACF, specificando il tipo di handle di associazione che rappresenta la connessione tra client e server. **\[** [**\_ L'attributo handle implicito**](/windows/desktop/Midl/implicit-handle) nell'intestazione ACF consente all'applicazione client di selezionare **\]** un server per la chiamata di procedura remota. L'ACF definisce l'handle per essere del tipo [**handle \_ t**](/windows/desktop/Midl/handle-t) (un tipo di dati primitivo MIDL). Il compilatore MIDL inserirà il nome dell'handle di associazione specificato dall'ACF, hello \_ IfHandle, nel file di intestazione generato. Si noti che questo particolare file ACF ha un corpo vuoto.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

Il compilatore MIDL ha un'opzione, [**/app \_ config**](/windows/desktop/Midl/-app-config), che consente di includere determinati attributi ACF, ad esempio **\_ handle implicito**, nel file IDL, anziché creare un file ACF separato. È consigliabile usare questa opzione se l'applicazione non richiede molte configurazioni speciali e se la compatibilità OSF rigida non rappresenta un problema.

 

 
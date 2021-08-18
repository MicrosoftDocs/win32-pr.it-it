---
title: The IDL File
description: Il file IDL è costituito da una o più definizioni di interfaccia, ognuna delle quali ha un'intestazione e un corpo.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f46a92fe5967dca1faeca1d658cf398fb0baf6ebd9160c3a736747de324e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924415"
---
# <a name="the-idl-file"></a>The IDL File

Il file IDL è costituito da una o più definizioni di interfaccia, ognuna delle quali ha un'intestazione e un corpo. L'intestazione contiene informazioni che si applicano all'intera interfaccia, ad esempio l'UUID. Queste informazioni sono racchiuse tra parentesi quadre ed è seguita dalla parola chiave **interface** e dal nome dell'interfaccia. Il corpo contiene definizioni di tipi di dati di tipo C e prototipi di funzione, arricchiti con attributi che descrivono come i dati vengono trasmessi in rete.

In questo esempio l'intestazione dell'interfaccia contiene solo l'UUID e il numero di versione. Il numero di versione garantisce che quando sono presenti più versioni di un'interfaccia RPC, verranno connesse solo le versioni compatibili del client e del server.

Il corpo dell'interfaccia contiene il prototipo di funzione **per HelloProc.** In questo prototipo il parametro della funzione pszString ha gli attributi **\[** [**in**](/windows/desktop/Midl/in) **\]** e la **\[** [**stringa**](/windows/desktop/Midl/string) **\]** . **\[ L'attributo in \]** indica alla libreria di runtime che il parametro viene passato solo dal client al server. **\[ L'attributo \]** string specifica che lo stub deve considerare il parametro come stringa di caratteri di tipo C.

L'applicazione client deve essere in grado di arrestare l'applicazione server, in modo che l'interfaccia contenga un prototipo per un'altra funzione remota,**Shutdown** , che verrà implementata più avanti in questa esercitazione.

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 
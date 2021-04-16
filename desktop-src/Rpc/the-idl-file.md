---
title: File IDL
description: Il file IDL è costituito da una o più definizioni di interfaccia, ognuna delle quali dispone di un'intestazione e di un corpo.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473294"
---
# <a name="the-idl-file"></a>File IDL

Il file IDL è costituito da una o più definizioni di interfaccia, ognuna delle quali dispone di un'intestazione e di un corpo. L'intestazione contiene informazioni che si applicano all'intera interfaccia, ad esempio l'UUID. Queste informazioni sono racchiuse tra parentesi quadre ed è seguita dall' **interfaccia** della parola chiave e dal nome dell'interfaccia. Il corpo contiene le definizioni del tipo di dati C e i prototipi di funzione, integrati con attributi che descrivono in che modo i dati vengono trasmessi in rete.

In questo esempio, l'intestazione dell'interfaccia contiene solo l'UUID e il numero di versione. Il numero di versione garantisce che, in presenza di più versioni di un'interfaccia RPC, verranno connesse solo le versioni compatibili del client e del server.

Il corpo dell'interfaccia contiene il prototipo di funzione per **HelloProc**. In questo prototipo, il parametro della funzione pszString ha gli attributi **\[** [**in**](/windows/desktop/Midl/in) **\]** e **\[** [**String**](/windows/desktop/Midl/string) **\]** . L'attributo **\[ in \]** indica alla libreria di runtime che il parametro viene passato solo dal client al server. L'attributo **\[ String \]** specifica che lo stub deve considerare il parametro come una stringa di caratteri di tipo C.

L'applicazione client deve essere in grado di arrestare l'applicazione server, quindi l'interfaccia contiene un prototipo per un'altra funzione remota,**Shutdown** , che verrà implementata più avanti in questa esercitazione.

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

 

 
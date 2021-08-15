---
title: Serializzazione dei tipi
description: Il compilatore MIDL genera fino a tre funzioni per ogni tipo a cui viene applicato l'attributo \ encode\ o \ decode\.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d898a077ff55bb03a76fbd7579e28a8bcdf18c792330b32b1eb832c6b9058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011099"
---
# <a name="type-serialization"></a>Serializzazione dei tipi

Il compilatore MIDL genera fino a tre funzioni per ogni tipo a cui viene applicato l'attributo di \[ [](/windows/desktop/Midl/encode) \] \[ [codifica](/windows/desktop/Midl/decode) \] o decodifica. Ad esempio, per un tipo definito dall'utente denominato *MyType*, il compilatore genera il codice per le funzioni MyType \_ Encode, MyType Decode e \_ MyType \_ AlignSize. Per queste funzioni, il compilatore scrive prototipi in Stub.h e codice sorgente in Stub \_ c.c. In genere, è possibile codificare un oggetto *MyType* con MyType Encode e decodificare un oggetto dal \_ buffer usando MyType \_ Decode. MyType \_ AlignSize viene usato se è necessario conoscere le dimensioni del buffer di marshalling prima di allocarlo.

La funzione di codifica seguente viene generata dal compilatore MIDL. Questa funzione serializza i dati per l'oggetto a cui punta pObject e il buffer viene ottenuto in base al metodo specificato nell'handle. Dopo aver scritto i dati serializzati nel buffer, è possibile controllare il buffer. Si noti che l'handle eredita lo stato dalle chiamate precedenti e i buffer devono essere allineati a 8.

Per un handle implicito:

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Per un handle esplicito:

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La funzione seguente deserializza i dati dalla memoria dell'applicazione nell'oggetto a cui punta pObject. Si fornisce un buffer di cui è stato effettuato il marshalling in base al metodo specificato nell'handle. Si noti che l'handle può ereditare lo stato dalle chiamate precedenti e i buffer devono essere allineati a 8.

Per un handle implicito:

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Per un handle esplicito:

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La funzione seguente restituisce una dimensione, in byte, che include l'istanza del tipo più eventuali byte di riempimento necessari per allineare i dati. Ciò consente la serializzazione di un set di istanze dello stesso tipo o di tipi diversi in un buffer, assicurando al tempo stesso che i dati per ogni oggetto siano allineati in modo appropriato. MyType AlignSize presuppone che l'istanza a cui punta pObject verrà sottoposto a marshalling in un buffer a partire \_ dall'offset allineato a 8.

Per un handle implicito:

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Per un handle esplicito:

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Si noti che entrambe le procedure remote con handle di associazione implicita e i tipi serializzati con handle di serializzazione implicita usano la stessa variabile di handle globale. È pertanto consigliabile non combinare la serializzazione dei tipi e le procedure remote in un'interfaccia con handle impliciti. Per informazioni dettagliate, vedere [Handle impliciti e espliciti.](implicit-versus-explicit-handles.md)

 

 
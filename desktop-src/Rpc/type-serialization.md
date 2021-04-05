---
title: Serializzazione del tipo
description: Il compilatore MIDL genera fino a tre funzioni per ogni tipo a cui viene applicato l'attributo \ Encode \ o \ Decode \.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674617bc98c92dbc684a29d1a3c91ac6a7429e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118054"
---
# <a name="type-serialization"></a>Serializzazione del tipo

Il compilatore MIDL genera fino a tre funzioni per ogni tipo a cui \[ [](/windows/desktop/Midl/encode) \] viene applicato l'attributo Encode o \[ [Decode](/windows/desktop/Midl/decode) \] . Ad esempio, per un tipo definito dall'utente denominato *MyType*, il compilatore genera il codice per le \_ funzioni MyType Encode, MyType \_ Decode e MyType \_ AlignSize. Per queste funzioni, il compilatore scrive i prototipi in Stub. h e il codice sorgente nello stub \_ c.c. In genere, è possibile codificare un oggetto *MyType* con \_ la codifica MyType e decodificare un oggetto dal buffer usando la \_ decodifica MyType. MyType \_ AlignSize viene usato se è necessario ottenere informazioni sulla dimensione del buffer di marshalling prima di allocarlo.

La funzione di codifica seguente viene generata dal compilatore MIDL. Questa funzione serializza i dati per l'oggetto a cui fa riferimento pObject e il buffer viene ottenuto in base al metodo specificato nell'handle. Dopo aver scritto i dati serializzati nel buffer, è possibile controllare il buffer. Si noti che l'handle eredita lo stato dalle chiamate precedenti e che i buffer devono essere allineati a 8.

Per un handle implicito:

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Per un handle esplicito:

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La funzione seguente deserializza i dati dalla risorsa di archiviazione dell'applicazione nell'oggetto a cui punta pObject. Si fornisce un buffer di cui è stato effettuato il marshalling in base al metodo specificato nell'handle. Si noti che l'handle può ereditare lo stato dalle chiamate precedenti e che i buffer devono essere allineati a 8.

Per un handle implicito:

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Per un handle esplicito:

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La funzione seguente restituisce una dimensione, in byte, che include l'istanza del tipo più tutti i byte di riempimento necessari per allineare i dati. In questo modo è possibile serializzare un set di istanze dello stesso tipo o di tipi diversi in un buffer garantendo al contempo che i dati per ogni oggetto siano allineati in modo appropriato. MyType \_ AlignSize presuppone che l'istanza a cui fa riferimento pObject venga sottoposta a marshalling in un buffer a partire dall'offset allineato a 8.

Per un handle implicito:

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Per un handle esplicito:

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Si noti che entrambe le procedure remote con handle di binding impliciti e tipi serializzati con handle di serializzazione implicite utilizzano la stessa variabile di handle globale. Pertanto, è consigliabile non combinare la serializzazione dei tipi e le procedure remote in un'interfaccia con handle impliciti. Per informazioni dettagliate, vedere [handle impliciti e espliciti](implicit-versus-explicit-handles.md).

 

 
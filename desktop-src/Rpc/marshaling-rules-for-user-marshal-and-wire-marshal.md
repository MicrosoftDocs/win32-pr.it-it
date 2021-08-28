---
title: Regole di marshalling per user_marshal e wire_marshal
description: La specifica OSF-DCE per il marshalling dei tipi di puntatore incorporati richiede di osservare le restrizioni seguenti quando si implementa il tipo UserSize, il tipo UserMarshal e le funzioni \_ \_ \_ UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97f073a5745570aae5c52d4a61d2454b960d77a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883829"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Regole di marshalling per il marshalling \_ dell'utente e il wire \_ marshal

La specifica OSF-DCE per il marshalling dei tipi di puntatore incorporati richiede di osservare le restrizioni seguenti quando si implementa il tipo UserSize, il tipo UserMarshal e le funzioni &lt; &gt; \_ &lt; &gt; \_ &lt; &gt; \_ UserUnMarshal. Le regole e gli esempi riportati di seguito sono relativi al marshalling. Tuttavia, le routine di ridimensionamento e unmarshaling devono rispettare le stesse restrizioni:

-   Se wire-type è un tipo flat senza puntatori, la routine di marshalling per il tipo userm corrispondente deve semplicemente effettuare il marshalling dei dati in base al layout del wire-type. Ad esempio:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Si noti che il tipo wire, **long,** è un tipo flat. La funzione HANDLE \_ \_ HANDLE UserMarshal effettua il marshalling di **un oggetto long** ogni volta che vi viene passato un oggetto HANDLE \_ HANDLE.

-   Se wire-type è un puntatore a un altro tipo, la routine di marshalling per il tipo userm corrispondente deve effettuare il marshalling dei dati in base al layout per il tipo a cui punta il tipo di collegamento. Il motore NDR si occupa del puntatore. Ad esempio:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Si noti che il tipo wire, **WIRE \_ TYPE,** è un tipo puntatore. La funzione HANDLE DATA UserMarshal effettua il marshalling dei dati correlati all'handle, usando il \_ \_ layout HDATA anziché il layout \* HDATA.

-   Un tipo wire deve essere un tipo di dati flat o un tipo di puntatore. Se il tipo trasmissibile deve essere diverso,ad esempio una struttura con puntatori, usare un puntatore al tipo desiderato come tipo di collegamento.

L'effetto di queste restrizioni è che i tipi definiti con gli attributi wire marshal o user marshal possono essere liberamente incorporati in \[ [**\_**](/windows/desktop/Midl/wire-marshal) \] altri \[ [**\_**](/windows/desktop/Midl/user-marshal) \] tipi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**wire \_ marshal**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**marshalling \_ utente**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Funzione \_ UserSize di tipo](the-type-usersize-function.md)
</dt> <dt>

[Funzione \_ UserMarshal di tipo](the-type-usermarshal-function.md)
</dt> <dt>

[Tipo \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[Tipo \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 

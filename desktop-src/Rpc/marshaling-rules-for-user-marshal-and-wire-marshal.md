---
title: Regole di marshalling per user_marshal e wire_marshal
description: La specifica OSF-DCE per il marshalling dei tipi di puntatore incorporato richiede di osservare le restrizioni seguenti quando si implementa il tipo \_ UserSize, digitare \_ UserMarshal e digitare \_ UserUnMarshal Functions.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728858"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Regole di marshalling per \_ marshalling utente e \_ marshalling di rete

La specifica OSF-DCE per il marshalling dei tipi di puntatore incorporato richiede di osservare le restrizioni seguenti quando si implementano le <type> \_ funzioni UserSize, <type> \_ UserMarshal e <type> \_ UserUnMarshal. (Le regole e gli esempi riportati di seguito sono per il marshalling. Tuttavia, le routine di ridimensionamento e di unmarshalling devono rispettare le stesse restrizioni:

-   Se il tipo Wire è un tipo Flat senza puntatori, la routine di marshalling per il tipo User-Type corrispondente dovrebbe semplicemente effettuare il marshalling dei dati in base al layout del tipo di Wire. Ad esempio:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Si noti che il tipo Wire, **Long**, è un tipo flat. Il gestore gestisce il \_ \_ marshalling della funzione UserMarshal a **lungo** ogni volta che un oggetto handle handle \_ viene passato a tale oggetto.

-   Se il tipo di Wire è un puntatore a un altro tipo, la routine di marshalling per il tipo di utente corrispondente deve effettuare il marshalling dei dati in base al layout per il tipo a cui punta il tipo di Wire. Il motore di NDR si occupa dell'indicatore di misura. Ad esempio:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Si noti che il tipo di **trasmissione \_ Wire è** un tipo di puntatore. La \_ funzione UserMarshal data di handle esegue il \_ marshalling dei dati correlati all'handle, usando il layout HDATA anziché il \* layout HDATA.

-   Un tipo di collegamento deve essere un tipo di dati flat o un tipo di puntatore. Se il tipo trasmissibile deve essere un altro elemento (una struttura con puntatori, ad esempio), usare un puntatore al tipo desiderato come tipo di collegamento.

L'effetto di queste restrizioni è che i tipi definiti con gli attributi di marshalling \[ [**\_**](/windows/desktop/Midl/wire-marshal) \] o di \[ [**\_ marshalling degli utenti**](/windows/desktop/Midl/user-marshal) \] possono essere incorporati liberamente in altri tipi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_marshalling di rete**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**\_marshalling utente**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Funzione di tipo \_ UserSize](the-type-usersize-function.md)
</dt> <dt>

[Funzione di tipo \_ UserMarshal](the-type-usermarshal-function.md)
</dt> <dt>

[\_UserUnMarshalFunction thetype](the-type-userunmarshal-function.md)
</dt> <dt>

[\_UserFreeFunction thetype](the-type-userfree-function.md)
</dt> </dl>

 

 
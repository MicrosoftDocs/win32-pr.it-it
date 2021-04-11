---
title: Decode (attributo)
description: L'attributo \ Decode \ ACF specifica che una routine o un tipo necessita del supporto di deserializzazione.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Decode attribute MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337167"
---
# <a name="decode-attribute"></a>Decode (attributo)

L'attributo **\[ Decode \]** ACF specifica che una routine o un tipo necessita del supporto di deserializzazione.

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica altri attributi che si applicano all'interfaccia nel suo complesso.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*interfaccia-definizione* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell'interfaccia.

</dd> <dt>

*op-Attribute-List* 
</dt> <dd>

Specifica altri attributi operativi che si applicano alla procedura, ad esempio **\[** [**Encode**](encode.md) **\]** .

</dd> <dt>

*proc-name* 
</dt> <dd>

Specifica il nome della stored procedure.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica altri attributi, ad esempio **\[** [**Encode**](encode.md) **\]** e **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*Nome-tipo* 
</dt> <dd>

Specifica un tipo definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Decode \]** induce il compilatore MIDL a generare codice che può essere utilizzato da un'applicazione per recuperare dati serializzati da un buffer. L' **\[** [](encode.md) **\]** attributo Encode fornisce supporto per la serializzazione, che genera il codice per serializzare i dati in un buffer.

Utilizzare gli **\[** attributi [**Encode**](encode.md) **\]** e **\[ Decode \]** in un oggetto ACF per generare il codice di serializzazione per le procedure o i tipi definiti nel file IDL di un'interfaccia. Quando viene usato come attributo di interfaccia, **\[ Decode \]** si applica a tutti i tipi e le procedure definiti nel file IDL. Quando viene usato come attributo di tipo, **\[ Decode \]** si applica solo al tipo specificato. Quando viene usato come attributo operativo, **\[ Decode \]** si applica solo a tale procedura.

Per ulteriori informazioni sull'utilizzo di questo supporto della serializzazione, vedere [serializzazione di servizi](/windows/desktop/Rpc/serialization-services) e **\[** [**codifica**](encode.md) **\]** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocare**](allocate.md)
</dt> <dt>

[**codificare**](encode.md)
</dt> </dl>

 

 
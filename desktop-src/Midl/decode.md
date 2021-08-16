---
title: Attributo decode
description: L'attributo \ decode\ ACF specifica che una procedura o un tipo deve supportare la deserializzazione.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Attributo decode MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30c70c821906bcfa4dedb8dbe87aab882866a4f21b7d561b16d3613f9041e0f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384727"
---
# <a name="decode-attribute"></a>Attributo decode

**\[ L'attributo \]** ACF di decodifica specifica che una routine o un tipo deve supportare la deserializzazione.

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

*interface-attribute-list* 
</dt> <dd>

Specifica altri attributi che si applicano all'interfaccia nel suo complesso.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell'interfaccia.

</dd> <dt>

*op-attribute-list* 
</dt> <dd>

Specifica altri attributi operativi che si applicano alla procedura, ad esempio **\[** [**encode**](encode.md) **\]** .

</dd> <dt>

*proc-name* 
</dt> <dd>

Specifica il nome della procedura.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica altri attributi, ad esempio **\[** [**codificare e**](encode.md) **\]** **\[** [**allocare**](allocate.md) **\]** .

</dd> <dt>

*type-name* 
</dt> <dd>

Specifica un tipo definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \] decode** fa sì che il compilatore MIDL generi codice che un'applicazione può usare per recuperare i dati serializzati da un buffer. **\[** [**L'attributo encode**](encode.md) **\]** fornisce supporto per la serializzazione, generando il codice per serializzare i dati in un buffer.

Usare gli **\[** [**attributi di**](encode.md) **\]** **\[ \]** codifica e decodifica in un file ACF per generare codice di serializzazione per routine o tipi definiti nel file IDL di un'interfaccia. Se usata come attributo di interfaccia, **\[ la decodifica \]** si applica a tutti i tipi e le routine definiti nel file IDL. Se usata come attributo di tipo, **\[ la decodifica \]** si applica solo al tipo specificato. Se usato come attributo operativo, **\[ la decodifica \]** si applica solo a tale procedura.

Per altre informazioni sull'uso di questo supporto di serializzazione, vedere [Servizi di serializzazione](/windows/desktop/Rpc/serialization-services) **\[** [**e codifica**](encode.md) **\]** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Allocare**](allocate.md)
</dt> <dt>

[**Codificare**](encode.md)
</dt> </dl>

 

 
---
title: void (attributo)
description: Il tipo di base void indica una routine senza argomenti o una routine che non restituisce un valore di risultato.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- attributo void MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299189"
---
# <a name="void-attribute"></a>void (attributo)

Il tipo di base **void** indica una routine senza argomenti o una routine che non restituisce un valore di risultato.

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Specifica l'elenco di parametri passati alla funzione insieme ai tipi di parametro e agli attributi dei parametri associati.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Specifica il nome del tipo restituito dalla funzione.

</dd> <dt>

*context-handle-tipo* 
</dt> <dd>

Specifica il nome del tipo che accetta l'attributo dell' **\[** [**\_ handle di contesto**](context-handle.md) **\]** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo di **puntatore \* void**, che in C descrive un puntatore generico di cui è possibile eseguire il cast per rappresentare qualsiasi tipo di puntatore, è limitato in MIDL al relativo utilizzo con la parola chiave dell' **\[ \_ handle \] di contesto** .

## <a name="examples"></a>Esempi

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 





---
title: Attributo void
description: Il tipo di base void indica una routine senza argomenti o una routine che non restituisce un valore di risultato.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- Attributo void MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad758ba334114e13493e7b082f45f37dc6e68efba16dc3a55f14fa57a772d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382437"
---
# <a name="void-attribute"></a>Attributo void

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

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Specifica l'elenco di parametri passati alla funzione insieme ai tipi di parametro e agli attributi dei parametri associati.

</dd> <dt>

*return-type* 
</dt> <dd>

Specifica il nome del tipo restituito dalla funzione.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Specifica il nome del tipo che accetta **\[** [**l'attributo \_ dell'handle di**](context-handle.md) **\]** contesto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo di puntatore void _, che in C descrive un puntatore generico di cui è possibile eseguire il cast per rappresentare qualsiasi tipo di puntatore, è limitato in MIDL all'uso con la parola chiave **\* *_* \[ context \_ handle. \]**

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

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 





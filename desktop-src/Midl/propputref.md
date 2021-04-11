---
title: propputref (attributo)
description: L'attributo \ propputref \ specifica una funzione di impostazione di proprietà che usa un riferimento invece di un valore.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- attributo MIDL di propputref
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956373"
---
# <a name="propputref-attribute"></a>propputref (attributo)

L'attributo **\[ propputref \]** specifica una funzione di impostazione di proprietà che usa un riferimento invece di un valore.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*facoltativo-Property-Attributes* 
</dt> <dd>

Zero o più attributi della proprietà.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Tipo di dati restituiti dalla procedura remota.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome della procedura remota.

</dd> <dt>

*parameters* 
</dt> <dd>

Zero o più parametri per la procedura remota.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una funzione con l'attributo **\[ propputref \]** deve avere anche l'ultimo parametro, ovvero un puntatore **\[** [**con l'attributo in**](in.md) **\]** .

La proprietà deve avere lo stesso nome della funzione. **\[** [](propget.md) **\]** **\[** [](propput.md) **\]** Per una funzione è possibile specificare al massimo uno degli attributi propget, propput e **\[ propputref \]** .

### <a name="flags"></a>Flags

RICHIAMA \_ PROPERTYPUTREF

## <a name="examples"></a>Esempi

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
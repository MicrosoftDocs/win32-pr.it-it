---
title: propget (attributo)
description: L'attributo \ propget \ specifica una funzione di accesso alla proprietà. La proprietà deve avere lo stesso nome della funzione.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- attributo MIDL di propget
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046588"
---
# <a name="propget-attribute"></a>propget (attributo)

L'attributo **\[ propget \]** specifica una funzione di accesso alla proprietà. La proprietà deve avere lo stesso nome della funzione.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
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

Una funzione con l'attributo propget deve avere anche l'ultimo parametro, un tipo di puntatore con gli **\[** attributi [**out**](out-idl.md) **\]** e **\[** [**retval**](retval.md) **\]** . Se l'ultimo parametro non dispone degli \[ attributi out, retval \] , il valore restituito della funzione viene considerato come un \[ parametro out, retval \] . Ad esempio, una funzione con il prototipo

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

viene considerato come

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

**\[ \]** **\[** [](propput.md) **\]** **\[** [](propputref.md) **\]** Per una funzione è possibile specificare al massimo uno dei propget, propput e propputref.

Se l' **\[** attributo [**LCID**](lcid.md) **\]** viene usato nell'elenco di parametri di una funzione che contiene un parametro con l' **\[** [](propput.md) **\]** attributo propput, il parametro **\[ LCID \]** deve essere il secondo all'ultimo.

### <a name="flags"></a>Flags

RICHIAMA \_ PropertyGet (

## <a name="examples"></a>Esempi

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
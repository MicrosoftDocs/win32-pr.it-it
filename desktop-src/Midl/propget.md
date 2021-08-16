---
title: propget (attributo)
description: L'attributo \ propget\ specifica una funzione di accesso alle proprietà. La proprietà deve avere lo stesso nome della funzione.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- Attributo propget MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa55521042adc07f4242a44060e2442f087e609d0e3995d8c77457c8653c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383336"
---
# <a name="propget-attribute"></a>propget (attributo)

**\[ L'attributo \] propget** specifica una funzione di accesso alle proprietà. La proprietà deve avere lo stesso nome della funzione.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*optional-property-attributes* 
</dt> <dd>

Zero o più attributi di proprietà.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo dei dati restituiti dalla procedura remota.

</dd> <dt>

*function-name* 
</dt> <dd>

Nome della procedura remota.

</dd> <dt>

*parameters* 
</dt> <dd>

Zero o più parametri per la procedura remota.

</dd> </dl>

## <a name="remarks"></a>Commenti

Anche una funzione con l'attributo propget deve avere, come ultimo parametro, un tipo di puntatore con gli **\[** [**attributi out**](out-idl.md) **\]** e **\[** [**retval.**](retval.md) **\]** Se l'ultimo parametro non ha gli attributi out e retval, il valore restituito della funzione viene considerato come parametro \[ \] \[ out, retval. \] Ad esempio, una funzione con il prototipo

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

viene considerato come

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

Al massimo, è possibile specificare uno tra **\[ \] propget**, **\[** [**propput**](propput.md) **\]** e **\[** [**propputref**](propputref.md) **\]** per una funzione.

Se **\[** [**l'attributo lcid**](lcid.md) viene utilizzato nell'elenco di parametri di una funzione che contiene un parametro con l'attributo propput, il parametro **\]** **\[** [](propput.md) **\]** **\[ lcid \]** deve essere il secondo all'ultimo.

### <a name="flags"></a>Flags

INVOKE \_ PROPERTYGET

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

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
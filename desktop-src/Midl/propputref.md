---
title: propputref (attributo)
description: L'attributo \ propputref\ specifica una funzione di impostazione delle proprietà che usa un riferimento anziché un valore.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- Attributo propputref MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e80b0baa4f78537142043b374c206ade0f3d51d7ca30c2f57e1c4ae4e9b695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641964"
---
# <a name="propputref-attribute"></a>propputref (attributo)

**\[ L'attributo \] propputref** specifica una funzione di impostazione delle proprietà che usa un riferimento anziché un valore.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
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

Anche una funzione con **\[ l'attributo propputref \]** deve avere, come ultimo parametro, un puntatore con l'attributo **\[** [**in**](in.md) **\]** .

La proprietà deve avere lo stesso nome della funzione. Al massimo, è possibile specificare uno degli attributi **\[** [**propget**](propget.md), propput e **\]** **\[** [](propput.md) **\]** **\[ propputref \]** per una funzione.

### <a name="flags"></a>Flags

INVOKE \_ PROPERTYPUTREF

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

[**Pollici**](in.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
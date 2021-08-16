---
title: propput (attributo)
description: L'attributo \ propput\ specifica una funzione di impostazione della proprietà. La proprietà deve avere lo stesso nome della funzione.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- Attributo propput MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e34d4826abfa2df6cd1262ccd4bcec04344f4500ddf5c146816d23f6261c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641934"
---
# <a name="propput-attribute"></a>propput (attributo)

**\[ L'attributo \] propput** specifica una funzione di impostazione della proprietà. La proprietà deve avere lo stesso nome della funzione *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*optional-property-attributes* 
</dt> <dd>

Zero o più attributi di proprietà.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo di dati restituiti dalla procedura remota.

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

Una funzione con **\[ l'attributo propput \]** deve avere anche, come ultimo parametro, un parametro con l'attributo **\[** [**in**](in.md) **\]** .

Al massimo, è possibile specificare uno dei valori **\[** [**propget**](propget.md) **\]** , **\[ propput \]** e **\[** [**propputref**](propputref.md) per una **\]** funzione.

Se **\[** [**l'attributo lcid**](lcid.md) viene usato nell'elenco di parametri di una funzione che contiene un parametro con l'attributo **\]** **\[ propput, \]** il **\[ parametro lcid \]** deve essere secondo all'ultimo.

### <a name="flags"></a>Flags

RICHIAMARE \_ PROPERTYPUT

## <a name="examples"></a>Esempi

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Differenze tra MIDL e MKTYPLIB](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
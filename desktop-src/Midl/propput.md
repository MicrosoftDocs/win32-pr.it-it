---
title: propput (attributo)
description: L'attributo \ propput \ specifica una funzione di impostazione di proprietà. La proprietà deve avere lo stesso nome della funzione.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- attributo MIDL di propput
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117611"
---
# <a name="propput-attribute"></a>propput (attributo)

L'attributo **\[ propput \]** specifica una funzione di impostazione di proprietà. La proprietà deve avere lo stesso nome della funzione *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
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

Una funzione con l'attributo **\[ propput \]** deve avere anche l'ultimo parametro, ovvero un parametro **\[** [**con l'attributo in**](in.md) **\]** .

**\[** [](propget.md) **\]** **\[ \]** **\[** [](propputref.md) **\]** Per una funzione è possibile specificare al massimo uno dei propget, propput e propputref.

Se l' **\[** attributo [**LCID**](lcid.md) **\]** viene usato nell'elenco di parametri di una funzione che contiene un parametro con l'attributo **\[ propput \]** , il parametro **\[ LCID \]** deve essere il secondo all'ultimo.

### <a name="flags"></a>Flags

RICHIAMA \_ PROPERTYPUT

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

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
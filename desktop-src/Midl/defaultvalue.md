---
title: defaultvalue (attributo)
description: L'attributo \defaultvalue\ consente di specificare un valore predefinito per un parametro facoltativo tipidato.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- Attributo defaultvalue MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f38fe7dfc99c5c9c1c6a7cae1a5fdd5750c5f3e9af37e56706b27300876da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067351"
---
# <a name="defaultvalue-attribute"></a>defaultvalue (attributo)

**\[ L'attributo \] defaultvalue** consente di specificare un valore predefinito per un parametro facoltativo tipidato.

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*return-type* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato **\[ l'attributo defaultvalue. \]**

</dd> <dt>

*mandatory-param-list* 
</dt> <dd>

Specifica uno o più parametri obbligatori.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al parametro .

</dd> <dt>

*param-type* 
</dt> <dd>

Indica il tipo del parametro facoltativo.

</dd> <dt>

*param-name* 
</dt> <dd>

Specifica il nome del parametro facoltativo.

</dd> <dt>

*optional-param-list* 
</dt> <dd>

Specifica zero o più parametri aggiuntivi, ognuno dei quali deve avere un valore predefinito.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore predefinito specificato per il parametro può essere qualsiasi costante o espressione che viene risolta in una costante, che può essere rappresentata da **variant.** In particolare, non è possibile applicare **\[ l'attributo defaultvalue \]** a un parametro che è una struttura, una matrice o un **tipo SAFEARRAY.**

Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):

1.  Parametri obbligatori (parametri che non hanno il **\[ valore predefinito o \]** attributi **\[** [**facoltativi),**](optional.md) **\]**
2.  parametri facoltativi con o senza **\[ l'attributo defaultvalue, \]**
3.  parametri con **\[ l'attributo facoltativo \]** e senza **\[ l'attributo defaultvalue, \]**
4.  **\[**[**Parametro lcid,**](lcid.md) **\]** se presente,
5.  **\[**[**retval**](retval.md) **\]** Parametro

## <a name="examples"></a>Esempi

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**Opzionale**](optional.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
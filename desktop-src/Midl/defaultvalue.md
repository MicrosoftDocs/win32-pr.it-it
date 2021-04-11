---
title: defaultvalue (attributo)
description: L'attributo \ DefaultValue \ consente di specificare un valore predefinito per un parametro facoltativo tipizzato.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- attributo DefaultValue MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337270"
---
# <a name="defaultvalue-attribute"></a>defaultvalue (attributo)

L'attributo **\[ DefaultValue \]** consente di specificare un valore predefinito per un parametro facoltativo tipizzato.

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

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato l'attributo **\[ DefaultValue \]** .

</dd> <dt>

*elenco di parametri obbligatori* 
</dt> <dd>

Specifica o più parametri obbligatori.

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al parametro.

</dd> <dt>

*param-Type* 
</dt> <dd>

Indica il tipo del parametro facoltativo.

</dd> <dt>

*nome param* 
</dt> <dd>

Specifica il nome del parametro facoltativo.

</dd> <dt>

*facoltativo-param-list* 
</dt> <dd>

Specifica zero o più parametri aggiuntivi, ognuno dei quali deve avere un valore predefinito.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore predefinito specificato per il parametro può essere qualsiasi costante oppure un'espressione che viene risolta in una costante, che può essere rappresentata da un **Variant**. In particolare, non è possibile applicare l'attributo **\[ \] DefaultValue** a un parametro che è una struttura, una matrice o un tipo **SAFEARRAY** .

Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):

1.  Parametri obbligatori (parametri che non dispongono degli attributi **\[ DefaultValue \]** o **\[** [**Optional**](optional.md) **\]** ),
2.  parametri facoltativi con o senza l'attributo **\[ DefaultValue \]** ,
3.  parametri con l'attributo **\[ facoltativo \]** e senza l'attributo **\[ DefaultValue \]** ,
4.  **\[** parametro [**LCID**](lcid.md) **\]** , se presente,
5.  **\[**[**retval**](retval.md) **\]** parametro

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

[**interfaccia**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**opzionale**](optional.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
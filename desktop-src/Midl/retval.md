---
title: retval (attributo)
description: L'attributo \ retval\ definisce il parametro che riceve il valore restituito del membro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- Attributo retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72655883b24c83890cf2f5604cb8f7335c6943b32e5e69611dba415689b03e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146304"
---
# <a name="retval-attribute"></a>retval (attributo)

**\[ L'attributo \] retval** definisce il parametro che riceve il valore restituito del membro.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*return-type* 
</dt> <dd>

Tipo di dati del valore restituito della procedura remota.

</dd> <dt>

*function-name* 
</dt> <dd>

Nome utilizzato per richiamare la procedura remota.

</dd> <dt>

*attributi facoltativi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo di dati* 
</dt> <dd>

Tipo di dati passati tramite il parametro .

</dd> <dt>

*param-name* 
</dt> <dd>

Nome dell'identificatore del parametro.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare **\[ l'attributo retval \]** sui parametri dei membri dell'interfaccia che descrivono metodi o ottengono proprietà. L'attributo è obbligatorio nell'ultimo parametro di un metodo con **\[** [**propget**](propget.md) **\]** attribute.) Il parametro deve avere **\[** [**l'attributo out**](out-idl.md) **\]** e deve essere un tipo puntatore.

Non è possibile applicare **\[** [**l'attributo**](optional.md) **\]** facoltativo a un **\[ parametro retval. \]**

Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):

1.  Parametri obbligatori (parametri che non hanno il **\[** [**valore predefinito**](defaultvalue.md) **\]** o attributi **\[** [**facoltativi).**](optional.md) **\]**
2.  Parametri facoltativi con o senza **\[** [**l'attributo**](defaultvalue.md) **\]** defaultvalue.
3.  Parametri con **\[** [**l'attributo facoltativo**](optional.md) **\]** e senza **\[** [**l'attributo defaultvalue.**](defaultvalue.md) **\]**
4.  **\[**[**Parametro lcid,**](lcid.md) **\]** se presente.
5.  **\[ parametro retval. \]**

I parametri con **\[ l'attributo retval \]** non vengono visualizzati nei browser orientati all'utente.

### <a name="flags"></a>Flags

IDLFLAG \_ FRETVAL

## <a name="examples"></a>Esempi

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Defaultvalue**](defaultvalue.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Opzionale**](optional.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
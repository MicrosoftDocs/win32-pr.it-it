---
title: retval (attributo)
description: L'attributo \ retval \ designa il parametro che riceve il valore restituito del membro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- attributo retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872358"
---
# <a name="retval-attribute"></a>retval (attributo)

L'attributo **\[ retval \]** designa il parametro che riceve il valore restituito del membro.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo restituito* 
</dt> <dd>

Tipo di dati del valore restituito della procedura remota.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome utilizzato per richiamare la procedura remota.

</dd> <dt>

*facoltativo-attributi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo di dati* 
</dt> <dd>

Tipo di dati passati tramite il parametro.

</dd> <dt>

*nome param* 
</dt> <dd>

Nome dell'identificatore del parametro.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare l'attributo **\[ retval \]** sui parametri dei membri di interfaccia che descrivono metodi o ottengono proprietà. L'attributo è obbligatorio per l'ultimo parametro di un metodo con il **\[** parametro [**propget**](propget.md) **\]** attributo). Il parametro deve avere l' **\[** attributo [**out**](out-idl.md) **\]** e deve essere un tipo di puntatore.

Non è possibile applicare l' **\[** attributo [**facoltativo**](optional.md) **\]** a un parametro **\[ \] retval** .

Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):

1.  Parametri obbligatori (parametri senza **\[** [](defaultvalue.md) **\]** attributi DefaultValue o **\[** [**facoltativi**](optional.md) **\]** ).
2.  Parametri facoltativi con o senza l' **\[** [](defaultvalue.md) **\]** attributo DefaultValue.
3.  Parametri con l' **\[** attributo [**facoltativo**](optional.md) **\]** e senza l' **\[** attributo [**DefaultValue**](defaultvalue.md) **\]** .
4.  **\[** parametro [**LCID**](lcid.md) **\]** , se disponibile.
5.  parametro **\[ retval \]** .

I parametri con l'attributo **\[ retval \]** non vengono visualizzati nei browser orientati agli utenti.

### <a name="flags"></a>Flags

\_FRETVAL IDLFLAG

## <a name="examples"></a>Esempi

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**opzionale**](optional.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
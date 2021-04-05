---
title: optional (attributo)
description: L'attributo \ optional \ specifica un parametro facoltativo per una funzione membro.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- attributo MIDL facoltativo
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872490"
---
# <a name="optional-attribute"></a>optional (attributo)

L'attributo **\[ facoltativo \]** specifica un parametro facoltativo per una funzione membro.

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo restituito* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*altri attributi* 
</dt> <dd>

Zero o più attributi MIDL facoltativi.

</dd> <dt>

*tipo di parametro* 
</dt> <dd>

Tipo di dati del parametro facoltativo.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica il nome del parametro facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ facoltativo \]** è valido solo se il parametro è di tipo **Variant** o **Variant** \* .

Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):

1.  Parametri obbligatori (parametri che non dispongono degli **\[** attributi [**DefaultValue**](defaultvalue.md) **\]** o **\[ Optional \]** ),
2.  Parametri facoltativi con o senza l' **\[** [](defaultvalue.md) **\]** attributo DefaultValue,
3.  Parametri con l'attributo **\[ facoltativo \]** e senza l' **\[** attributo [**DefaultValue**](defaultvalue.md) **\]** ,
4.  **\[** parametro [**LCID**](lcid.md) **\]** , se presente,
5.  **\[**[**retval**](retval.md) **\]** parametro

Non è possibile applicare l'attributo **\[ facoltativo \]** a un parametro che include anche gli **\[** attributi [**LCID**](lcid.md) **\]** o **\[** [**retval**](retval.md) **\]** .

## <a name="examples"></a>Esempi

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
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

[**retval**](retval.md)
</dt> </dl>

 

 
---
title: vararg (attributo)
description: L'attributo \ vararg \ specifica che la funzione accetta un numero variabile di parametri. A tale scopo, l'ultimo parametro deve essere una matrice sicura di tipo VARIANT che contiene tutti i parametri rimanenti.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- attributo MIDL di vararg
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299752"
---
# <a name="vararg-attribute"></a>vararg (attributo)

L'attributo **\[ vararg \]** specifica che la funzione accetta un numero variabile di parametri. A tale scopo, l'ultimo parametro deve essere una matrice sicura di tipo **Variant** che contiene tutti i parametri rimanenti.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*facoltativo-attributi* 
</dt> <dd>

Specifica zero o più attributi da applicare alla funzione. Separare più attributi con virgole.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Tipo di dati restituiti dalla procedura remota al termine del processo.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome della procedura remota.

</dd> <dt>

*facoltativo-param-Attributes* 
</dt> <dd>

Specifica zero o più attributi da applicare al parametro della funzione immediatamente dopo l'elenco degli attributi.

</dd> <dt>

*param-list* 
</dt> <dd>

Specifica tutti i parametri, Salva il parametro finale, variabile.

</dd> <dt>

*Last-param-name* 
</dt> <dd>

Nome del parametro variabile.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non è possibile applicare gli **\[** attributi [**facoltativi**](optional.md) **\]** o **\[** [**DefaultValue**](defaultvalue.md) **\]** a tutti i parametri in una funzione con l'attributo **\[ vararg \]** .

## <a name="examples"></a>Esempi

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**opzionale**](optional.md)
</dt> </dl>

 

 
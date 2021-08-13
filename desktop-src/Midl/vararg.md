---
title: vararg (attributo)
description: L'attributo \ vararg\ specifica che la funzione accetta un numero variabile di parametri. A tale scopo, l'ultimo parametro deve essere una matrice sicura di tipo VARIANT che contiene tutti i parametri rimanenti.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- Attributo vararg MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848393f6bad82d6793e34ba6f4da803c7dd64803c1c40e4ea05487ea141ec48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641009"
---
# <a name="vararg-attribute"></a>vararg (attributo)

**\[ L'attributo \] vararg** specifica che la funzione accetta un numero variabile di parametri. A tale scopo, l'ultimo parametro deve essere una matrice sicura di tipo **VARIANT** che contiene tutti i parametri rimanenti.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attributi facoltativi* 
</dt> <dd>

Specifica zero o più attributi da applicare alla funzione. Separare più attributi con virgole.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo di dati restituiti dalla procedura remota al completamento.

</dd> <dt>

*function-name* 
</dt> <dd>

Nome della procedura remota.

</dd> <dt>

*optional-param-attributes* 
</dt> <dd>

Specifica zero o più attributi da applicare al parametro della funzione immediatamente dopo l'elenco di attributi.

</dd> <dt>

*param-list* 
</dt> <dd>

Specifica tutti i parametri e salva il parametro finale, variabile.

</dd> <dt>

*last-param-name* 
</dt> <dd>

Nome del parametro varying.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non è possibile applicare **\[** [**gli attributi**](optional.md) **\]** **\[** [**facoltativi o defaultvalue**](defaultvalue.md) ad alcun parametro in una **\]** **\[ \] funzione con l'attributo vararg.**

## <a name="examples"></a>Esempi

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Defaultvalue**](defaultvalue.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Opzionale**](optional.md)
</dt> </dl>

 

 
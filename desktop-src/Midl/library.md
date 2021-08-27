---
title: Attributo library
description: L'istruzione library contiene tutte le informazioni utilizzate dal compilatore MIDL per generare una libreria dei tipi.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- attributo della libreria MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc1f836174a57f6edfddd0575a10d40367c061c034369a1582cc8bf8ce17a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086371"
---
# <a name="library-attribute"></a>Attributo library

**L'istruzione** library contiene tutte le informazioni utilizzate dal compilatore MIDL per generare una libreria dei tipi.

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione universalmente univoco per la libreria.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica attributi aggiuntivi che si applicano all'intera istruzione **della** libreria. Gli attributi consentiti includono il controllo **\[** [](control.md) **\]** , **\[** [**helpcontext**](helpcontext.md) **\]** , **\[** [**helpfile**](helpfile.md), **\]** **\[** [**helpstring**](helpstring.md), **\]** **\[** [**hidden**](hidden.md) **\]** , **\[** [**lcid**](lcid.md), **\]** **\[** [**restricted**](restricted.md)e **\]** **\[** [**version**](version.md) **\]** .

</dd> <dt>

*nome-libreria* 
</dt> <dd>

Nome con cui i componenti software fanno riferimento alla **libreria**.

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono il contenuto della **libreria**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le istruzioni all'interno del blocco di libreria possono usare elementi dichiarati all'interno o all'esterno del blocco di libreria. Le istruzioni della libreria possono usare tali elementi come tipi di base, ereditando da tali elementi o semplicemente facendo riferimento a tali elementi in una riga, come indicato di seguito:

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

Il compilatore MIDL creerà una libreria dei tipi che include le definizioni per ogni elemento all'interno del blocco di libreria, oltre alle definizioni per tutti gli elementi definiti all'esterno e a cui si fa riferimento all'interno del blocco di libreria.

Per informazioni sulla generazione di una libreria dei tipi e di stub proxy e intestazioni da un singolo file IDL, vedere [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Contenuto di una libreria dei tipi](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Controllo**](control.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Nascosto**](hidden.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Limitato**](restricted.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 
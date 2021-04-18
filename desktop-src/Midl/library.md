---
title: attribute Library
description: L'istruzione Library contiene tutte le informazioni utilizzate dal compilatore MIDL per generare una libreria dei tipi.
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
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299788"
---
# <a name="library-attribute"></a>attribute Library

L'istruzione **Library** contiene tutte le informazioni utilizzate dal compilatore MIDL per generare una libreria dei tipi.

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

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la libreria.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica gli attributi aggiuntivi che si applicano all'intera istruzione della **libreria** . Gli attributi consentiti includono **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**filelima**](helpfile.md), **\]** **\[** [**helpstring**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** e **\[** [**Version**](version.md) **\]** .

</dd> <dt>

*nome della libreria* 
</dt> <dd>

Nome con cui i componenti software fanno riferimento alla **libreria**.

</dd> <dt>

*Library-Definition-Statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono il contenuto della **libreria**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le istruzioni all'interno del blocco di libreria possono usare elementi dichiarati all'interno o all'esterno del blocco di libreria. Le istruzioni Library possono usare tali elementi come tipi di base, ereditando da tali elementi o semplicemente facendo riferimento a essi su una riga, come indicato di seguito:

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

Il compilatore MIDL creerà una libreria dei tipi che include le definizioni per ogni elemento all'interno del blocco Library, più le definizioni per tutti gli elementi definiti all'esterno e a cui viene fatto riferimento dall'interno del blocco di libreria.

Per informazioni sulla generazione di una libreria dei tipi e di stub e intestazioni proxy da un singolo file IDL, vedere [generazione di una DLL proxy e di una libreria dei tipi da un singolo file IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).

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

[**controllo**](control.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**nascosto**](hidden.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**limitato**](restricted.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 
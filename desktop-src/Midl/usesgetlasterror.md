---
title: usesgetlasterror (attributo)
description: L'attributo \ usesgetlasterror\ segnala al chiamante che può chiamare GetLastError per recuperare il codice di errore.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- attributo usesgetlasterror MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239486792eb218d51c305f9955331e90c6c165586153dab167f2e19d3a0324e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641036"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror (attributo)

**\[ L'attributo usesgetlasterror \]** segnala al chiamante che può chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore.

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*module-attributes* 
</dt> <dd>

Zero o più attributi MIDL che verranno applicati al [**modulo**](module.md).

</dd> <dt>

*module-name* 
</dt> <dd>

Nome dell'identificatore del [**modulo**](module.md).

</dd> <dt>

*entry-id* 
</dt> <dd>

Specifica il nome del punto di ingresso del modulo o il numero di identificazione integer.

</dd> <dt>

*altri attributi* 
</dt> <dd>

Zero o più attributi MIDL che verranno applicati alla procedura remota.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo di dati restituiti dalla procedura remota al completamento.

</dd> <dt>

*function-name* 
</dt> <dd>

Nome della procedura remota come definito nel file IDL.

</dd> <dt>

*param-list* 
</dt> <dd>

Zero o più parametri per la procedura remota.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo usesgetlasterror \]** può essere impostato su un punto di ingresso del modulo, se tale punto di ingresso usa la funzione [**setLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) Windows per restituire i codici di errore. L'attributo indica al chiamante che, se si verifica un errore durante la chiamata a tale funzione, il chiamante può quindi chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore.

## <a name="examples"></a>Esempi

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 
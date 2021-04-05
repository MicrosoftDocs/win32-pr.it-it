---
title: usesgetlasterror (attributo)
description: L'attributo \ usesgetlasterror \ segnala al chiamante che è possibile chiamare GetLastError per recuperare il codice di errore.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- attributo MIDL di usesgetlasterror
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725138"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror (attributo)

L'attributo **\[ \] usesgetlasterror** segnala al chiamante che è possibile chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore.

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

*Module-attributi* 
</dt> <dd>

Zero o più attributi MIDL che verranno applicati al [**modulo**](module.md).

</dd> <dt>

*nome modulo* 
</dt> <dd>

Nome dell'identificatore del [**modulo**](module.md).

</dd> <dt>

*ID di ingresso* 
</dt> <dd>

Specifica il punto di ingresso del modulo, ovvero il nome della funzione o il numero di identificazione intero.

</dd> <dt>

*altri attributi* 
</dt> <dd>

Zero o più attributi MIDL che verranno applicati alla procedura remota.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Tipo di dati che la procedura remota restituirà al completamento.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome della procedura remota come definito nel file IDL.

</dd> <dt>

*param-list* 
</dt> <dd>

Zero o più parametri per la procedura remota.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile impostare l'attributo **\[ \] usesgetlasterror** in un punto di ingresso del modulo, se tale punto di ingresso usa la funzione di Windows [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire i codici di errore. L'attributo indica al chiamante che, se si verifica un errore durante la chiamata a tale funzione, il chiamante può quindi chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore.

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

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 
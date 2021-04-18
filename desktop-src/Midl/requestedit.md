---
title: requestedit (attributo)
description: L'attributo \ requestedit \ indica che la proprietà supporta la notifica OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- attributo MIDL di requestedit
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299632"
---
# <a name="requestedit-attribute"></a>requestedit (attributo)

L'attributo **\[ \] requestedit** indica che la proprietà supporta la notifica **OnRequestEdit** .

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*facoltativo-attributi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zero o più parametri di funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il supporto della notifica **OnRequestEdit** significa che, prima che venga apportata una modifica, l'oggetto invierà al client una richiesta di autorizzazione per la modifica di una proprietà. Un oggetto può supportare data binding ma non avere questo attributo.

### <a name="flags"></a>Flags

FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT

## <a name="examples"></a>Esempi

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
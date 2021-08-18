---
title: Attributo helpstringdll
description: L'attributo \ helpstringdll\ imposta il nome della DLL da usare per eseguire una ricerca di stringhe di documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- Attributo helpstringdll MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f773ed18e72f184305275ce238ddf0576c81447181a0b7fb420c30341935f5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067251"
---
# <a name="helpstringdll-attribute"></a>Attributo helpstringdll

**\[ L'attributo helpstringdll \]** imposta il nome della DLL da usare per eseguire una ricerca di stringhe di documento.

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*help-text-string* 
</dt> <dd>

Stringa di caratteri con terminazione zero che specifica il nome file completo di una DLL.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Altri attributi applicabili all'intera istruzione library.

</dd> <dt>

*library-name* 
</dt> <dd>

Identificatore che verrà utilizzato da componenti software per indicare questa [**libreria.**](library.md)

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono l'interfaccia della [**libreria**](library.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare **\[ l'attributo \] helpstringdll** in un'istruzione library per specificare, come stringa di caratteri, il nome file completo di una libreria a collegamento dinamico. Ciò consente a un utente di visualizzare una descrizione della DLL con il visualizzatore oggetti.

Usare le **funzioni GetDocumentation2** nelle **interfacce ITypeLib2** e **ITypeInfo2** per recuperare la stringa della Guida.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Libreria**](library.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
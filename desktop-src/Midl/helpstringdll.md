---
title: attributo helpstringdll
description: L'attributo \ helpstringdll \ imposta il nome della DLL da usare per eseguire una ricerca di stringhe di documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- attributo MIDL di helpstringdll
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956396"
---
# <a name="helpstringdll-attribute"></a>attributo helpstringdll

L'attributo **\[ helpstringdll \]** imposta il nome della dll da usare per eseguire una ricerca di stringhe di documento.

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

*Guida-testo-stringa* 
</dt> <dd>

Stringa di caratteri con terminazione zero che specifica il nome di file completo di una DLL.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Altri attributi applicabili all'intera istruzione della libreria.

</dd> <dt>

*nome della libreria* 
</dt> <dd>

Identificatore che i componenti software utilizzeranno per indicare la [**libreria**](library.md).

</dd> <dt>

*Library-Definition-Statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono l'interfaccia della [**libreria**](library.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Utilizzare l'attributo **\[ helpstringdll \]** in un'istruzione Library per specificare, come stringa di caratteri, il nome file completo di una libreria a collegamento dinamico. Questo consente a un utente di visualizzare una descrizione della DLL con il Visualizzatore oggetti.

Usare le funzioni **GetDocumentation2** nelle interfacce **ITypeLib2** e **ITypeInfo2** per recuperare la stringa della guida.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**libreria**](library.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
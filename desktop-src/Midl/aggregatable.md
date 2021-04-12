---
title: aggregatable (attributo)
description: L'attributo \ aggregable \ indica che la classe supporta l'aggregazione.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- MIDL attributo aggregabile
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337086"
---
# <a name="aggregatable-attribute"></a>aggregatable (attributo)

L'attributo **\[ aggregable \]** indica che la classe supporta l'aggregazione.

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Altri attributi che si applicano alla classe.

</dd> <dt>

*coclass-nome* 
</dt> <dd>

Nome della classe.

</dd> <dt>

*coclass-interface-List* 
</dt> <dd>

Elenco di interfacce per la classe.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare l'attributo **\[ aggregable \]** in un'istruzione [**coclass**](coclass.md) per informare gli utenti che la classe supporta le aggregazioni. Ovvero la classe consente l'esposizione delle interfacce da parte di una classe contenitore come se queste interfacce fossero interfacce del contenitore.

La rappresentazione TypeFlag per questo attributo è TYPEFLAG \_ FAGGREGATABLE.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 
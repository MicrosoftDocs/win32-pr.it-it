---
title: noncreatable (attributo)
description: L'attributo \ noncreatable\ definisce un oggetto di cui non è possibile creare un'istanza da solo.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- ATTRIBUTO MIDL non creabile
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e59c53d8e4c05d15d55a6ccd9d7fb2b5cd8783463d1f59d439c74240fdd93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066941"
---
# <a name="noncreatable-attribute"></a>noncreatable (attributo)

**\[ L'attributo \] non creabile** definisce un oggetto di cui non è possibile creare un'istanza da solo.

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

Altri attributi che si applicano alla classe .

</dd> <dt>

*coclass-name* 
</dt> <dd>

Nome della classe.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Elenco di interfacce per la classe.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare **\[ l'attributo \] noncreatable** in un'istruzione [**di coclasse**](coclass.md) per indicare agli utenti che non possono creare un nuovo oggetto di questa classe al livello superiore, ovvero chiamando **CreateInstance** o **CoCreateInstance**. La creazione di un'istanza di un oggetto di questa classe richiede una chiamata al metodo a un altro oggetto. Ad esempio, in Microsoft Excel l'oggetto "Cell" non è creabile e deve essere ottenuto da un Microsoft Excel Worksheet.

I metodi che restituiscono istanze di classi non creabili devono restituire il tipo esatto dell'oggetto, anziché i tipi **VARIANT** **o IDispatch.** \*

### <a name="typeflag-representation"></a>Rappresentazione typeflag:

Assenza di TYPEFLAG \_ FCANCREATE.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
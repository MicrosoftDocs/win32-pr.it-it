---
title: noncreatable (attributo)
description: L'attributo \ noncreable \ definisce un oggetto di cui non è possibile creare un'istanza.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- attributo MIDL non creabile
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337039"
---
# <a name="noncreatable-attribute"></a>noncreatable (attributo)

L'attributo non generabile definisce un oggetto di cui non è possibile creare un'istanza. **\[ \]**

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

Usare l'attributo **\[ noncreable \]** in un'istruzione [**coclass**](coclass.md) per indicare agli utenti che non possono creare un nuovo oggetto di questa classe al livello principale, ovvero chiamando **CreateInstance** o **CoCreateInstance**. La creazione di un'istanza di un oggetto di questa classe richiede una chiamata al metodo a un altro oggetto. In Microsoft Excel, ad esempio, l'oggetto "Cell" non è creabile e deve essere ottenuto da un oggetto foglio di lavoro di Microsoft Excel.

I metodi che restituiscono istanze di classi non creabili devono restituire il tipo esatto dell'oggetto, anziché i tipi **Variant** o **IDispatch** \* .

### <a name="typeflag-representation"></a>Rappresentazione TypeFlag:

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

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
---
title: attributo personalizzato
description: L'attributo \ custom \ crea un attributo definito dall'utente.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- MIDL attributo personalizzato
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299602"
---
# <a name="custom-attribute"></a>attributo personalizzato

L'attributo **\[ Custom \]** crea un attributo definito dall'utente.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ID attributo* 
</dt> <dd>

GUID per l'attributo personalizzato.

</dd> <dt>

*valore attributo* 
</dt> <dd>

Valore che l'attributo include. Il valore deve essere un valore che può essere inserito in un tipo VARIANT.

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Altri attributi, ad esempio **\[** [**UUID**](uuid.md) **\]** e **\[** [**helpstring**](helpstring.md) **\]** , che si applicano a questo elemento.

</dd> <dt>

*tipo di elemento* 
</dt> <dd>

Tipo di elemento a cui viene applicato l'attributo personalizzato. Può trattarsi di un'istruzione di libreria, informazioni sul tipo, una variabile, una funzione o un parametro. Non è possibile usare un attributo personalizzato per un membro di una coclasse.

</dd> <dt>

*Nome elemento* 
</dt> <dd>

Nome dell'elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare l'attributo personalizzato per definire un attributo **\[ personalizzato \]** . Ad esempio, è possibile creare un attributo con valori di stringa che fornisce il ProgID per una classe.

Per recuperare un valore di attributo personalizzato, chiamare uno dei seguenti:

-   ITypeLib2:: GetCustData (rguid, pvarVal)
-   ITypeInfo2:: GetCustData (rguid, pvarVal)
-   ITypeInfo2:: GetFuncCustData (index, rguid, pvarVal)
-   ITypeInfo2:: GetVarCustData (index, rguid, pVarVal)
-   ITypeInfo2:: GetParamCustData (indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**libreria**](library.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 
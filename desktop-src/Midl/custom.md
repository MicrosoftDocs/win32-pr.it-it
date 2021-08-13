---
title: attributo personalizzato
description: L'attributo \custom\ crea un attributo definito dall'utente.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- attributo personalizzato MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace6a558da428da07a432653391e0e48b7a5545bb1a83eb40d9c950abfa9d9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643670"
---
# <a name="custom-attribute"></a>attributo personalizzato

**\[ L'attributo \]** personalizzato crea un attributo definito dall'utente.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attribute-id* 
</dt> <dd>

GUID per l'attributo personalizzato.

</dd> <dt>

*attribute-value* 
</dt> <dd>

Valore che l'attributo contiene. Il valore deve essere uno che può essere inserito in un tipo VARIANT.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Altri attributi, ad esempio **\[** [**uuid**](uuid.md) **\]** e **\[** [**helpstring**](helpstring.md) **\]** , che si applicano a questo elemento.

</dd> <dt>

*element-type* 
</dt> <dd>

Tipo di elemento a cui si applica l'attributo personalizzato. Può trattarsi di un'istruzione di libreria, informazioni sul tipo, una variabile, una funzione o un parametro. Non è possibile usare un attributo personalizzato su un membro di una coclasse.

</dd> <dt>

*element-name* 
</dt> <dd>

Nome dell'elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare **\[ l'attributo \]** personalizzato per definire un attributo personalizzato. Ad esempio, è possibile creare un attributo con valori stringa che fornisce il ProgID per una classe.

Per recuperare un valore di attributo personalizzato, chiamare uno dei metodi seguenti:

-   ITypeLib2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)
-   ITypeInfo2::GetVarCustData(index, rguid, pvarval)
-   ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Libreria**](library.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 
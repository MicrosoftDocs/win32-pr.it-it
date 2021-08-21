---
title: iid_is (attributo)
description: L'attributo del puntatore \ iid \_ is\ specifica l'IID dell'interfaccia COM a cui punta un puntatore di interfaccia.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is attributo MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74553fdb1e3020d49eca7dfdd219354a4690056c45126b3af208395117ade991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383868"
---
# <a name="iid_is-attribute"></a>iid \_ is attribute

**\[ L'attributo \_ \] iid is** pointer specifica l'IID dell'interfaccia COM a cui punta un puntatore di interfaccia.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*limited-expression* 
</dt> <dd>

Specifica un'espressione in linguaggio C. Il compilatore MIDL supporta espressioni condizionali, logiche, relazionali ed aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare **\[ iid negli elenchi \_ di \]** attributi per i parametri di funzione e per i membri di struttura o unione. Gli stub usano l'IID per determinare come effettuare il marshalling del puntatore a interfaccia. Ciò è utile per un puntatore a interfaccia tipivato come parametro della classe base.

I file che usano **\[ l'attributo iid \_ is \]** devono essere compilati con il compilatore MIDL in modalità predefinita, che non usa l'opzione [**/osf.**](-osf.md)

## <a name="examples"></a>Esempi

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Oggetto**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 





---
title: iid_is (attributo)
description: L'attributo \ IID \_ is \ Pointer indica l'IID dell'interfaccia com a cui punta un puntatore a interfaccia.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- attributo iid_is MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045572"
---
# <a name="iid_is-attribute"></a>IID \_ è un attributo

L' **\[ IID \_ è \]** un attributo puntatore che specifica l'IID dell'interfaccia com a cui punta un puntatore di interfaccia.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*espressione limitata* 
</dt> <dd>

Specifica un'espressione del linguaggio C. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile utilizzare **\[ IID \_ \]** negli elenchi di attributi per i parametri di funzione e per i membri della struttura o dell'Unione. Gli stub usano l'IID per determinare come eseguire il marshalling del puntatore a interfaccia. Questa operazione è utile per un puntatore a interfaccia tipizzato come parametro della classe di base.

I file che usano l' **\[ IID \_ sono \]** attributi devono essere compilati con il compilatore MIDL in modalità predefinita, che non usa l'opzione [**/OSF**](-osf.md) .

## <a name="examples"></a>Esempi

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**oggetto**](object.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 





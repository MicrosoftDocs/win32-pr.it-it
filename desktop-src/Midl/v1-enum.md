---
title: v1_enum (attributo)
description: L'attributo \ v1 enum\ indica che il tipo enumerato specificato viene trasmesso come entità a 32 bit, anziché come valore predefinito \_ a 16 bit.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum attributo MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7afb814cde879f0ada5124b1a19d8ac8b8c851deafcda7e75295a6e5338f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382785"
---
# <a name="v1_enum-attribute"></a>Attributo di enumerazione v1 \_

**\[ L'attributo \_ \] di** enumerazione v1 indica che il tipo enumerato specificato viene trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parametri

Questo attributo non ha parametri.

## <a name="remarks"></a>Commenti

L'uso dell'attributo **\[ \_ \] di** enumerazione v1 per trasmettere un tipo enumerato come entità a 32 bit aumenta l'efficienza del marshalling e dell'unmarsaling dei dati quando tale enumerazione è incorporata in strutture o unioni.

Per migliorare le prestazioni, è consigliabile applicare l'attributo **\[ \_ \] di enumerazione v1** agli enumeratori nelle applicazioni a 32 bit. Tenere presente, tuttavia, che nelle piattaforme a 16 bit il compilatore C considera un tipo enumerato come [**int**](int.md)a 16 bit. Le applicazioni client a 16 bit devono pertanto convertire i tipi [**enum**](enum.md) in [**long**](long.md) per la trasmissione remota per evitare la sovrascrittura dei dati o l'invio di valori non corretti.

## <a name="examples"></a>Esempi

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> </dl>

 

 





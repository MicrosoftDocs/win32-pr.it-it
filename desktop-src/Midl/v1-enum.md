---
title: v1_enum (attributo)
description: L'attributo \ V1 \_ enum \ indica che il tipo enumerato specificato deve essere trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- attributo v1_enum MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857438"
---
# <a name="v1_enum-attribute"></a>\_attributo enum V1

L'attributo **\[ \_ enum \] V1** indica che il tipo enumerato specificato deve essere trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parametri

Questo attributo non ha parametri.

## <a name="remarks"></a>Commenti

L'utilizzo dell'attributo **\[ \_ enum \] V1** per la trasmissione di un tipo enumerato come entità a 32 bit aumenta l'efficienza del marshalling e dell'unmarshalling dei dati quando tale enumerazione è incorporata in strutture o unioni.

Per migliorare le prestazioni, è consigliabile applicare l'attributo **\[ \_ enum \] V1** agli enumeratori nelle applicazioni a 32 bit. Tenere presente, tuttavia, che nelle piattaforme a 16 bit il compilatore C considera un tipo enumerato come [**int**](int.md)a 16 bit. Pertanto, le applicazioni client a 16 bit devono convertire i tipi [**enum**](enum.md) in [**Long**](long.md) per la trasmissione remota, in modo da evitare la sovrascrittura dei dati o l'invio di valori non corretti.

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

[**enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> </dl>

 

 





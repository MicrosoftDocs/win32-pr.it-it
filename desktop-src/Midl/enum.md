---
title: Attributo enum
description: L'enumerazione della parola chiave identifica un tipo enumerato.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- Attributo enum MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1519e6208e8bccae0288d6e0b31d7897faba4e1c9c7add8987f5dd493f4f5f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384490"
---
# <a name="enum-attribute"></a>Attributo enum

**L'enumerazione della parola chiave** identifica un tipo enumerato.

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tag* 
</dt> <dd>

Specifica un tag facoltativo per il tipo enumerato.

</dd> <dt>

*identifier* 
</dt> <dd>

Specifica l'enumerazione specifica.

</dd> <dt>

*valore intero* 
</dt> <dd>

Specifica un valore intero costante.

</dd> </dl>

## <a name="remarks"></a>Commenti

**I tipi enum** possono essere visualizzati come identificatori di tipo in dichiarazioni [**typedef,**](typedef.md) dichiarazioni generali e dichiaratori di funzione (come function-return-type o come identificatore di tipo parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [File di definizione dell'interfaccia (IDL).](interface-definition-idl-file.md)

Nella modalità predefinita del compilatore MIDL è possibile assegnare valori interi agli enumeratori. Questa funzionalità non è disponibile quando si esegue la compilazione con [**l'opzione /osf.**](-osf.md) Come per gli enumeratori in linguaggio C, i nomi degli enumeratori devono essere univoci, ma non è necessario che i valori dell'enumeratore lo siano.

Quando gli operatori di assegnazione non vengono specificati, viene eseguito il mapping degli identificatori a numeri interi consecutivi da sinistra a destra, a partire da zero. Quando vengono specificati gli operatori di assegnazione, i valori assegnati iniziano dal valore assegnato più di recente.

Il numero massimo di identificatori è 65.535.

Gli oggetti di **tipo enum** [**sono tipi int**](int.md) e le relative dimensioni dipendono dal sistema. Per impostazione predefinita, gli oggetti **dei tipi enum** vengono considerati come oggetti a 16 bit di tipo [**unsigned**](unsigned.md) [**short**](short.md) quando vengono trasmessi in rete. I valori non compreso nell'intervallo compreso tra 0 e 32.767 causano l'eccezione di run-time RPC \_ X \_ ENUM \_ VALUE OUT \_ \_ OF \_ RANGE. Per trasmettere oggetti come entità a 32 bit, applicare l'attributo **\[** [**\_ enum v1**](v1-enum.md) **\]** al typedef **enum.**

## <a name="examples"></a>Esempi

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**Enumerazione \_ v1**](v1-enum.md)
</dt> </dl>

 

 





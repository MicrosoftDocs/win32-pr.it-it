---
title: attributo enum
description: La parola chiave enum identifica un tipo enumerato.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- attributo di enumerazione MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333588"
---
# <a name="enum-attribute"></a>attributo enum

La parola chiave **enum** identifica un tipo enumerato.

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

Specifica l'enumerazione particolare.

</dd> <dt>

*valore integer* 
</dt> <dd>

Specifica un valore intero costante.

</dd> </dl>

## <a name="remarks"></a>Commenti

i tipi **enum** possono apparire come identificatori di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come funzione-Return-Type o come identificatore di tipo parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

Nella modalità predefinita del compilatore MIDL è possibile assegnare valori integer agli enumeratori. Questa funzionalità non è disponibile quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) . Come per gli enumeratori del linguaggio C, i nomi degli enumeratori devono essere univoci, ma i valori di enumeratore non devono essere.

Quando gli operatori di assegnazione non vengono specificati, viene eseguito il mapping degli identificatori a numeri interi consecutivi da sinistra a destra, a partire da zero. Quando vengono specificati gli operatori di assegnazione, i valori assegnati iniziano dal valore assegnato più di recente.

Il numero massimo di identificatori è 65.535.

Gli oggetti di tipo **enum** sono tipi [**int**](int.md) e le relative dimensioni sono dipendenti dal sistema. Per impostazione predefinita, gli oggetti di tipi **enum** vengono considerati oggetti a 16 bit di tipo [**unsigned**](unsigned.md) [**short**](short.md) quando vengono trasmessi in rete. I valori non compresi nell'intervallo compreso tra 0 e 32.767 determinano il valore dell'enumerazione RPC X dell'eccezione in fase di esecuzione non \_ \_ compreso nell' \_ \_ \_ \_ intervallo. Per trasmettere oggetti come entità a 32 bit, applicare l' **\[** [**attributo \_ enum V1**](v1-enum.md) **\]** al typedef **enum** .

## <a name="examples"></a>Esempi

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> <dt>

[**\_enum V1**](v1-enum.md)
</dt> </dl>

 

 





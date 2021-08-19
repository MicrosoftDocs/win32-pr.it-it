---
title: Attributo int
description: La parola chiave int specifica un intero con segno a 32 bit su piattaforme a 32 bit. Nelle piattaforme a 16 bit la parola chiave int è una parola chiave facoltativa che può accompagnare le parole chiave small, short e long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- Attributo int MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 640eae8bfbadcba07f67d244edd78726269ede9eee2f14e9af06e851bb5cac92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807199"
---
# <a name="int-attribute"></a>Attributo int

La parola **chiave int** specifica un intero con segno a 32 bit su piattaforme a 32 bit. Nelle piattaforme a 16 bit la parola chiave **int** è una parola chiave facoltativa che può accompagnare le parole chiave [**small**](small.md), [**short**](short.md)e [**long**](long.md).

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*modificatore integer* 
</dt> <dd>

Specifica la parola chiave [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)o [**\_ \_ int64**](--int64.md), che seleziona le dimensioni dei dati integer. Nelle piattaforme a 16 bit deve essere presente il qualificatore delle dimensioni.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrice. I dichiaratori di funzione e le dichiarazioni di campo di bit non sono consentiti nelle strutture trasmesse nelle chiamate di procedura remota. Questi dichiaratori sono consentiti nelle strutture che non vengono trasmesse. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

I tipi integer sono tra i tipi di base del linguaggio IDL (Interface Definition Language). Possono essere visualizzati come identificatori di tipo nelle dichiarazioni [**typedef,**](typedef.md) nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore function-return-type e come identificatore di tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [File di definizione dell'interfaccia (IDL).](interface-definition-idl-file.md)

Se non viene specificata alcuna specifica di segno integer, per impostazione predefinita il tipo integer è [**signed**](signed.md).

I compilatori IDL DCE non consentono alla parola chiave [**signed**](signed.md) di specificare il segno di tipi Integer. Pertanto, questa funzionalità non è disponibile quando si usa l'opzione [**/osf del**](-osf.md) compilatore MIDL.

Microsoft sconsiglia l'uso di \_ \_ int3264 per la comunicazione remota, se possibile. Per altre informazioni sull'uso e sulle limitazioni, vedere l'argomento relativo a [**\_ \_ int3264.**](--int3264.md)

## <a name="examples"></a>Esempi

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**hyper**](hyper.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Firmato**](signed.md)
</dt> <dt>

[**Piccolo**](small.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 





---
title: attributo int
description: La parola chiave int specifica un intero con segno a 32 bit sulle piattaforme a 32 bit. Nelle piattaforme a 16 bit la parola chiave int è una parola chiave facoltativa che può accompagnare le parole chiave Small, short e Long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- attributo int MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718064"
---
# <a name="int-attribute"></a>attributo int

La parola chiave **int** specifica un intero con segno a 32 bit sulle piattaforme a 32 bit. Nelle piattaforme a 16 bit la parola chiave **int** è una parola chiave facoltativa che può accompagnare le parole chiave [**small**](small.md), [**short**](short.md)e [**Long**](long.md).

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*modificatore Integer* 
</dt> <dd>

Specifica la parola chiave [**small**](small.md), [**short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)o [**\_ \_ Int64**](--int64.md), che consente di selezionare le dimensioni dei dati Integer. Nelle piattaforme a 16 bit è necessario che il qualificatore delle dimensioni sia presente.

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote. Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

I tipi integer sono tra i tipi di base del linguaggio di definizione dell'interfaccia (IDL). Possono apparire come identificatori di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

Se non viene specificata alcuna specifica del segno integer, l'impostazione predefinita del tipo Integer è [**signed**](signed.md).

I compilatori IDL DCE non consentono alla parola chiave [**signed**](signed.md) di specificare il segno dei tipi Integer. Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.

\_ \_ Se può essere evitato, Microsoft non consiglia l'uso di int3264 per la comunicazione remota. Per ulteriori informazioni sull'utilizzo e sulle limitazioni, vedere l'argomento relativo a [**\_ \_ int3264**](--int3264.md) .

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

[**enum**](enum.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**con segno**](signed.md)
</dt> <dt>

[**piccolo**](small.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Unione**](union.md)
</dt> </dl>

 

 





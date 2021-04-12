---
title: attributo booleano
description: La parola chiave booleana indica che l'espressione o l'espressione costante associata all'identificatore accetta solo i valori TRUE e FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- attributo booleano MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397811"
---
# <a name="boolean-attribute"></a>attributo booleano

La parola chiave **booleana** indica che l'espressione o l'espressione costante associata all'identificatore accetta solo i valori **true** e **false**.

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo **booleano** è uno dei tipi di base del linguaggio IDL. Il tipo **booleano** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

> [!Note]  
> Il tipo di base **booleano** non è compatibile con l'attributo [**oleautomation**](oleautomation.md) . Usare VARIANT \_ bool nelle interfacce compatibili con l'automazione.

 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 





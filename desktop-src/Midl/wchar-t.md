---
title: attributo wchar_t
description: La \_ parola chiave wchar t designa un tipo di carattere wide.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- attributo wchar_t MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2020
ms.locfileid: "104046400"
---
# <a name="wchar_t-attribute"></a>WCHAR \_ t (attributo)

La parola chiave **WCHAR \_ t** designa un tipo di carattere wide.

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo **WCHAR \_ t** viene definito da MIDL come oggetto dati [**short**](short.md) [**senza segno**](unsigned.md) (a 16 bit).

Il compilatore MIDL consente la ridefinizione di **WCHAR \_ t**, ma solo se è coerente con la definizione precedente.

Il tipo di carattere wide è uno dei tipi predefiniti di MIDL. Il tipo di carattere wide può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito della funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

L'attributo **\[ stringa \]** può essere applicato a un puntatore o a una matrice di tipo **WCHAR \_ t**.

Usare il carattere **L** prima di un carattere o una costante di stringa per definire la costante del tipo di carattere wide.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> </dl>

 

 





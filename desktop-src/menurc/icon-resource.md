---
title: ICONA risorsa
description: Definisce una bitmap che definisce la forma dell'icona da usare per una determinata applicazione o un'icona animata.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ICONA menu risorse e altre risorse
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516732"
---
# <a name="icon-resource"></a>ICONA risorsa

Definisce una bitmap che definisce la forma dell'icona da usare per una determinata applicazione o un'icona animata.

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o valore di Unsigned Integer a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente. Il percorso deve essere una stringa racchiusa tra virgolette.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

Le risorse icona e cursore possono contenere più di un'immagine.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono definite due risorse icona:

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle icone](./using-icons.md)
</dt> </dl>

 

 
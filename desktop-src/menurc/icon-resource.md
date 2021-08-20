---
title: Risorsa ICONA
description: Definisce una bitmap che definisce la forma dell'icona da usare per una determinata applicazione o un'icona animata.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- Menu delle risorse ICON e altre risorse
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2819d068f26433562ccb30369792af37b67f7d9dc78d1344988f60c699528e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687702"
---
# <a name="icon-resource"></a>Risorsa ICONA

Definisce una bitmap che definisce la forma dell'icona da usare per una determinata applicazione o un'icona animata.

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*Nameid*
</dt> <dd>

Nome univoco o valore intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente. Il percorso deve essere una stringa tra virgolette.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

Le risorse icona e cursore possono contenere più di un'immagine.

## <a name="examples"></a>Esempio

L'esempio seguente definisce due risorse icona:

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle icone](./using-icons.md)
</dt> </dl>

 

 
---
title: Risorsa cursore
description: Definisce una bitmap che definisce la forma del cursore sulla schermata di visualizzazione o su un cursore animato.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menu delle risorse del cursore e altre risorse
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299682"
---
# <a name="cursor-resource"></a>Risorsa cursore

Definisce una bitmap che definisce la forma del cursore sulla schermata di visualizzazione o su un cursore animato.

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o Unsigned Integer a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente. Il percorso deve essere una stringa racchiusa tra virgolette.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

Le risorse icona e cursore possono contenere più di un'immagine.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono definite due risorse cursore. uno per nome (Cursor1) e l'altro per numero (2):

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dei cursori](./using-cursors.md)
</dt> </dl>

 

 
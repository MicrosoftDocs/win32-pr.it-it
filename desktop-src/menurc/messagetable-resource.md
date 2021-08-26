---
title: Risorsa MESSAGETABLE
description: Definisce l'ID e il file della risorsa tabella messaggi di un'applicazione. Le tabelle dei messaggi sono risorse stringa speciali usate nella registrazione degli eventi e con la funzione FormatMessage. Il file contiene una tabella di messaggi binari generata dal compilatore di messaggi, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- Menu delle risorse MESSAGETABLE e altre risorse
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378860e10ab6da929147e13a8120ee169204276e3c609b20176c22df9de15dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886721"
---
# <a name="messagetable-resource"></a>Risorsa MESSAGETABLE

Definisce l'ID e il file della risorsa tabella messaggi di un'applicazione. Le tabelle dei messaggi sono risorse stringa speciali usate nella registrazione degli eventi e con la [**funzione FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) Il file contiene una tabella di messaggi binari generata dal compilatore di messaggi, MC.EXE.

Il compilatore di messaggi genera anche un file script di risorse che contiene le **istruzioni MESSAGETABLE** necessarie per includere le risorse della tabella dei messaggi nel file di risorse compilato. Usare la [**\# direttiva include**](-include.md) per includere questo script di risorsa nello script della risorsa principale.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*Nameid*
</dt> <dd>

Nome univoco o valore intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. Deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse.](common-resource-attributes.md)

## <a name="examples"></a>Esempio

L'esempio seguente definisce una **risorsa MESSAGETABLE:**

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 
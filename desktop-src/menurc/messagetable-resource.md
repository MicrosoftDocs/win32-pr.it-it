---
title: Risorsa MESSAGETABLE
description: Definisce l'ID e il file della risorsa della tabella dei messaggi di un'applicazione. Le tabelle dei messaggi sono risorse di stringa speciali utilizzate nella registrazione degli eventi e con la funzione FormatMessage. Il file contiene una tabella di messaggi binari generata dal compilatore di messaggi, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- Menu risorse MESSAGETABLE e altre risorse
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36281f7f6415465a6741f461574bca29c681cbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725551"
---
# <a name="messagetable-resource"></a>Risorsa MESSAGETABLE

Definisce l'ID e il file della risorsa della tabella dei messaggi di un'applicazione. Le tabelle dei messaggi sono risorse di stringa speciali utilizzate nella registrazione degli eventi e con la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . Il file contiene una tabella di messaggi binari generata dal compilatore di messaggi, MC.EXE.

Il compilatore di messaggi genera anche un file script di risorsa che contiene le istruzioni **MESSAGETABLE** necessarie per includere le risorse della tabella dei messaggi nel file di risorse compilato. Usare la direttiva [**\# include**](-include.md) per includere questo script di risorsa nello script della risorsa principale.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o valore di Unsigned Integer a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Nome del file che contiene la risorsa. Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene definita una risorsa **MESSAGETABLE** :

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 
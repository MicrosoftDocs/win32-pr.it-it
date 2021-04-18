---
description: Specifica il tipo di collegamento durante la ricerca per indicizzazione o l'indicizzazione.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Enumerazione LINKTYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306158"
---
# <a name="linktype-enumeration"></a>Enumerazione LINKTYPE

\[L'enumerazione **LinkType** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.\]

Specifica il tipo di collegamento durante la ricerca per indicizzazione o l'indicizzazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**\_URL LinkType**
</dt> <dd>

Specifica se il tipo di collegamento URL deve essere indicizzato.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**contenuto di LINKTYPE \_**
</dt> <dd>

Specifica se il contenuto del collegamento deve essere indicizzato.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**correlate a LINKTYPE \_**
</dt> <dd>

Specifica un collegamento correlato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare i flag **LinkType** e le altre API seguenti: i metodi [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e la struttura [**LINKINFO**](-search-linkinfo.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 





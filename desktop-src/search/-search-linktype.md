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
ms.openlocfilehash: 16c61f8d92a6f90be0fa4b64ddd9d582987ac0bdf52ca1c596c7db3a7fa4b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463044"
---
# <a name="linktype-enumeration"></a>Enumerazione LINKTYPE

\[**L'enumerazione LINKTYPE** è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.\]

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

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE \_ URL**
</dt> <dd>

Specifica se il tipo di collegamento URL deve essere indicizzato.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**CONTENUTO \_ LINKTYPE**
</dt> <dd>

Specifica se il contenuto del collegamento deve essere indicizzato.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE \_ CORRELATO**
</dt> <dd>

Specifica un collegamento correlato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare i flag **LINKTYPE** e le altre API seguenti: i metodi [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e la [**struttura LINKINFO.**](-search-linkinfo.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



 

 





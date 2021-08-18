---
description: Archivia informazioni sui tipi di collegamento e viene usato dall'interfaccia IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Struttura LINKINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97c106a5a819ac1068501c77555f3eae238c935e2262894c6c250dfc6782188f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863944"
---
# <a name="linkinfo-structure"></a>Struttura LINKINFO

\[**LINKINFO** e [**IItemPreviewerExt**](-search-iitempreviewerext.md) sono supportati solo in Windows XP e Windows Server 2003 e non devono più essere usati.\]

Archivia informazioni sui tipi di collegamento e viene usato [**dall'interfaccia IItemPreviewerExt.**](-search-iitempreviewerext.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**type**
</dt> <dd>

Tipo: **[ **LINKTYPE**](-search-linktype.md)**

</dd> <dd>

Tipo di collegamento specificato durante la ricerca per indicizzazione o l'indicizzazione indicata da una [**costante LINKTYPE.**](-search-linktype.md)

</dd> <dt>

**bstrContentType**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valore **BSTR** che specifica il tipo di contenuto.

</dd> <dt>

**bstrEncoding**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Attributo EncodingStyle specificato nel file Web Services Description Language (WSDL).

</dd> <dt>

**bstrFileExt**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valore **BSTR** che specifica l'estensione di file.

</dd> <dt>

**varData**
</dt> <dd>

Tipo: **VARIANT**

</dd> <dd>

Variante che specifica il valore della variabile.

</dd> <dt>

**dwRelatedParts**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valore **DWORD** che specifica le parti correlate.

</dd> <dt>

**bstrRelatedCid**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valore **BSTR** che specifica una proprietà Cid, una stringa decimale senza riempimento con segno.

</dd> <dt>

**lCodePage**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Tabella codici da utilizzare per la codifica della stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare la struttura **LINKINFO** e le API seguenti: i metodi [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



 

 





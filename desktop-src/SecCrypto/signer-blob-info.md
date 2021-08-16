---
description: Specifica un BLOB da firmare.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: SIGNER_BLOB_INFO struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a865a65b5fd9a1ec658dcc86b1eb2b3dd255804308f04bebf4fffdb0650d71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898928"
---
# <a name="signer_blob_info-structure"></a>Struttura SIGNER \_ BLOB \_ INFO

\[La **struttura SIGNER \_ BLOB \_ INFO** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La **struttura SIGNER \_ BLOB \_ INFO** specifica un [*BLOB*](../secgloss/b-gly.md) da firmare.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura .

</dd> <dt>

**pGuidSubject**
</dt> <dd>

Puntatore a un **GUID** che specifica il pacchetto DELL (Subject Interface Package) da caricare.

</dd> <dt>

**cbBlob**
</dt> <dd>

Dimensione, in byte, del BLOB da firmare.

</dd> <dt>

**pbBlob**
</dt> <dd>

Puntatore al BLOB da firmare.

</dd> <dt>

**pwszDisplayName**
</dt> <dd>

Nome visualizzato del BLOB. Questo membro può essere impostato su **NULL.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SUL \_ SOGGETTO DEL \_ FIRMATARIO**](signer-subject-info.md)
</dt> </dl>

 

 

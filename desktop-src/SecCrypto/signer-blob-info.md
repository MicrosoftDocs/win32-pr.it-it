---
description: Specifica un BLOB da firmare.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Struttura SIGNER_BLOB_INFO
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
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530289"
---
# <a name="signer_blob_info-structure"></a>Struttura di \_ informazioni BLOB del firmatario \_

\[La struttura delle **\_ \_ informazioni BLOB del firmatario** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La struttura di **\_ \_ informazioni BLOB del firmatario** specifica un [*BLOB*](../secgloss/b-gly.md) da firmare.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

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

Dimensione, in byte, della struttura.

</dd> <dt>

**pGuidSubject**
</dt> <dd>

Puntatore a un **GUID** che specifica il SIP (Subject Interface Package) da caricare.

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

Nome visualizzato del BLOB. Questo membro può essere impostato su **null**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**informazioni sul soggetto del FIRMATARIo \_ \_**](signer-subject-info.md)
</dt> </dl>

 

 

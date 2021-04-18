---
description: Specifica un oggetto da firmare.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Struttura SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310936"
---
# <a name="signer_subject_info-structure"></a>Struttura delle \_ informazioni sul soggetto del firmatario \_

La struttura delle **\_ \_ informazioni sul soggetto del firmatario** specifica un oggetto da firmare.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**pdwIndex**
</dt> <dd>

Questo membro è riservato. Deve essere impostato su zero.

</dd> <dt>

**dwSubjectChoice**
</dt> <dd>

Specifica se l'oggetto è un file o un [*BLOB*](../secgloss/b-gly.md). Il membro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                         | Significato                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**\_ Firmatario OGGETTO \_ BLOB**</dt> <dt>2 (0x2)</dt> </dl> | Il soggetto è un BLOB.<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**\_ Firmatario \_File oggetto**</dt> <dt>1 (0x1)</dt> </dl> | Il soggetto è un file.<br/> |



 

</dd> <dt>

**pSignerFileInfo**
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni sul file del firmatario**](signer-file-info.md) che specifica il file da firmare.

</dd> <dt>

**pSignerBlobInfo**
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni BLOB del firmatario**](signer-blob-info.md) che specifica il BLOB da firmare.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 

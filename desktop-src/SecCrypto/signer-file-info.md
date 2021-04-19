---
description: Specifica un file da firmare.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Struttura SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317693"
---
# <a name="signer_file_info-structure"></a>Struttura di \_ informazioni sul file del firmatario \_

La struttura di **\_ \_ informazioni sul file del firmatario** specifica un file da firmare.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**pwszFileName**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del file da firmare.

</dd> <dt>

**hFile**
</dt> <dd>

Handle aperto per il file specificato dal membro **pwszFileName** . Se questo membro contiene un handle valido, questo handle viene utilizzato per accedere al file. Questo membro può essere impostato su **null**.

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

 

 





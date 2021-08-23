---
description: Specifica un file da firmare.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: SIGNER_FILE_INFO struttura
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
ms.openlocfilehash: b0bb1bce810d87d70e05284e3d13942c5e2e49d07bd2d829c3839f793ae6a061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898827"
---
# <a name="signer_file_info-structure"></a>Struttura SIGNER \_ FILE \_ INFO

La **struttura SIGNER \_ FILE \_ INFO** specifica un file da firmare.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

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

Dimensione, in byte, della struttura .

</dd> <dt>

**pwszFileName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che contiene il nome del file da firmare.

</dd> <dt>

**hFile**
</dt> <dd>

Handle aperto per il file specificato dal **membro pwszFileName.** Se questo membro contiene un handle valido, questo handle viene usato per accedere al file. Questo membro può essere impostato su **NULL.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SUL SOGGETTO \_ DEL \_ FIRMATARIO**](signer-subject-info.md)
</dt> </dl>

 

 





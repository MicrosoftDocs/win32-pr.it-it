---
title: Struttura BG_FILE_RANGE (Deliveryoptimization. h)
description: La struttura BG_FILE_RANGE identifica un intervallo di byte da scaricare da un file.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Struttura BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400841"
---
# <a name="bg_file_range-structure"></a>Struttura BG_FILE_RANGE

La struttura **BG_FILE_RANGE** identifica un intervallo di byte da scaricare da un file.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>Members

<dl> <dt>

**InitialOffset**
</dt> <dd>

Offset in base zero all'inizio dell'intervallo di byte da scaricare da un file.

</dd> <dt>

**Length**
</dt> <dd>

Lunghezza dell'intervallo, in byte. Non specificare una lunghezza pari a zero byte. Per indicare che l'intervallo si estende fino alla fine del file, specificare **BG_LENGTH_TO_EOF**.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'intervallo deve esistere nel file o generare un errore di **DO_E_INVALID_RANGE** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile2::GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 






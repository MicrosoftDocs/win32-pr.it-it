---
title: Struttura STOWED_EXCEPTION_INFORMATION_HEADER
description: Contiene informazioni che identificano la struttura padre.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- Struttura STOWED_EXCEPTION_INFORMATION_HEADER Segnalazione errori Windows
- Puntatore alla struttura PSTOWED_EXCEPTION_INFORMATION_HEADER Segnalazione errori Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048672"
---
# <a name="stowed_exception_information_header-structure"></a>\_Struttura dell' \_ intestazione delle informazioni sulle eccezioni riposte \_

Contiene informazioni che identificano la struttura padre.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Dimensione, in byte, della struttura padre.

</dd> <dt>

**Firma**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore a 32 bit che specifica la firma della struttura padre.



| Valore                                                                                                                                                                                                                                                                                                            | Significato                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> Ricollocato <dt>**\_ \_Informazioni sull'eccezione \_ V1 \_ firma**</dt> <dt>' SE01'</dt> </dl> | Questo valore indica che l'elemento padre è una struttura di **\_ \_ informazioni sull' \_ eccezione ristivata** .<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> Ricollocato <dt>**\_ \_Informazioni sull'eccezione \_ v2 \_ firma**</dt> <dt>' SE02'</dt> </dl> | Questo valore indica che l'elemento padre è una struttura di [**\_ \_ informazioni sull' \_ eccezione ristivata V2**](stowed-exception-information-v2.md) .<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Ricollocato [**\_ \_Le informazioni sull'eccezione \_ v2**](stowed-exception-information-v2.md) e l' **\_ \_ \_ intestazione delle informazioni sulle eccezioni** riposte non sono attualmente definite in un'intestazione disponibile pubblicamente, pertanto è necessario definirle nel codice sorgente prima di utilizzarle.

La struttura di **\_ \_ informazioni \_ sull'eccezione ristivata** è identica a questa struttura, ad eccezione del fatto che non contiene i membri **NestedExceptionType** e **annidaexception** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Informazioni sulle eccezioni riposte \_ \_ v2**](stowed-exception-information-v2.md)
</dt> </dl>

 


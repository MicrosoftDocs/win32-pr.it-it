---
title: Struttura WINBIO_VERSION ( \_ tipi WINBIO. h)
description: Contiene il numero di versione del software di un componente del provider di servizi biometrico.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- Struttura di WINBIO_VERSION Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_VERSION
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479126"
---
# <a name="winbio_version-structure"></a>Struttura della versione di WINBIO \_

La struttura della **\_ versione WINBIO** contiene il numero di versione del software di un componente del provider di servizi biometrico.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>Members

<dl> <dt>

**MajorVersion**
</dt> <dd>

**Valore DWORD** che contiene il numero di versione principale.

</dd> <dt>

**MinorVersion**
</dt> <dd>

**Valore DWORD** che contiene il numero di versione secondario.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**\_schema BSP \_ WINBIO**](winbio-bsp-schema.md)
</dt> <dt>

[**\_schema unità \_ WINBIO**](winbio-unit-schema.md)
</dt> </dl>

 

 






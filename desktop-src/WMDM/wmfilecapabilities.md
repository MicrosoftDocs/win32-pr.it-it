---
title: Struttura WMFILECAPABILITIES
description: La struttura WMFILECAPABILITIES descrive il tipo MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Struttura WMFILECAPABILITIES Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324757"
---
# <a name="wmfilecapabilities-structure"></a>Struttura WMFILECAPABILITIES

La struttura **WMFILECAPABILITIES** descrive il tipo MIME.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Members

<dl> <dt>

**pwszMimeType**
</dt> <dd>

Tipo MIME.

</dd> <dt>

**dwReserved**
</dt> <dd>

**DWORD** riservato per un utilizzo futuro. Impostato su zero (0).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 






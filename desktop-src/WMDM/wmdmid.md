---
title: Struttura WMDMID
description: La struttura WMDMID descrive i numeri di serie e gli ID di gruppo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Struttura WMDMID Windows Media Gestione dispositivi
- Puntatore alla struttura PWMDMID Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332689"
---
# <a name="wmdmid-structure"></a>Struttura WMDMID

La struttura **WMDMID** descrive i numeri di serie e gli ID di gruppo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura **WMDMID** in byte.

</dd> <dt>

**dwVendorID**
</dt> <dd>

**DWORD** contenente il numero ID registrato del fornitore. Contiene zero se non è in uso.

</dd> <dt>

**\[lunghezza WMDMID \_ PID\]**
</dt> <dd>

Puntatore a una matrice di byte che contiene il numero di serie. Il numero di serie è una stringa di valori di byte privi di formato standard. Si noti che non si tratta di un valore a caratteri wide. **WMDMID \_ LENGTH** è un valore costante definito in mswmdm. h.

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

Lunghezza effettiva del numero di serie restituito, in byte.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPDevice:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**IWMDMDevice:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 






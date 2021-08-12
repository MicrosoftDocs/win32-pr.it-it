---
title: Struttura WMDMID
description: La struttura WMDMID descrive i numeri di serie e gli ID gruppo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Struttura WMDMID di Gestione dispositivi multimediali di Windows
- Puntatore alla struttura PWMDMID windows Media Device Manager
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
ms.openlocfilehash: 93079b2b32dae918e1c7f5c7756a1c24dd29c539c6b760dc698273006ae30f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583994"
---
# <a name="wmdmid-structure"></a>Struttura WMDMID

La **struttura WMDMID** descrive i numeri di serie e gli ID gruppo.

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

Dimensioni della **struttura WMDMID,** in byte.

</dd> <dt>

**dwVendorID**
</dt> <dd>

**Valore DWORD** contenente il numero ID registrato del fornitore. Contiene zero se non è in uso.

</dd> <dt>

**pID \[ WMDMID \_ LENGTH\]**
</dt> <dd>

Puntatore a una matrice di byte contenente il numero di serie. Il numero di serie è una stringa di valori di byte che non hanno un formato standard. Si noti che non si tratta di un valore a caratteri wide. **WMDMID \_ LENGTH** è un valore costante definito in mswmdm.h.

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

Lunghezza effettiva del numero di serie restituito, in byte.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**IWMDMDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 






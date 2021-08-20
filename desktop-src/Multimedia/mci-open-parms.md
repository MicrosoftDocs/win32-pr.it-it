---
title: MCI_OPEN_PARMS struttura (Mciapi.h)
description: La struttura MCI \_ OPEN \_ PARMS contiene informazioni per il comando MCI \_ OPEN.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80d01f41db904cea583f83aa446e718d1067e99e4d8bac3a3c6791ef5696f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138306"
---
# <a name="mci_open_parms-structure"></a>Struttura MCI \_ OPEN \_ PARMS

La **struttura MCI \_ OPEN \_ PARMS** contiene informazioni per il [**comando MCI \_ OPEN.**](mci-open.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificatore restituito all'applicazione.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nome o identificatore costante del tipo di dispositivo. Il nome del dispositivo viene in genere ottenuto dal registro o dal SYSTEM.INI file. Se questo membro è una costante, può essere uno dei valori elencati in [Tipi di dispositivo MCI.](mci-device-types.md)

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Elemento Device (spesso un percorso).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias del dispositivo facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 


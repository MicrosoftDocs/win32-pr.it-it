---
title: MCI_OVLY_OPEN_PARMS struttura (Mmsystem.h)
description: La struttura MCI OVLY OPEN PARMS contiene informazioni per \_ \_ il comando \_ MCI OPEN per i dispositivi di \_ sovrapposizione video.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f13d0e9f8a7a4b9f5477459286bc56b9c98b1f9564e8432329681aeaef66d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138277"
---
# <a name="mci_ovly_open_parms-structure"></a>Struttura MCI \_ OVLY \_ OPEN \_ PARMS

La **struttura MCI \_ OVLY \_ OPEN \_ PARMS** contiene informazioni per il [**comando MCI \_ OPEN**](mci-open.md) per i dispositivi di sovrapposizione video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificatore restituito all'applicazione.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nome o identificatore costante del tipo di dispositivo. Il nome del dispositivo viene in genere ottenuto dal Registro di sistema o SYSTEM.INI file. Se questo membro è una costante, può essere uno dei valori elencati in [McI Device Types](mci-device-types.md).

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nome dell'elemento dispositivo (in genere un percorso).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias dispositivo facoltativo.

</dd> <dt>

**dwStyle**
</dt> <dd>

Stile della finestra.

</dd> <dt>

**hWndParent**
</dt> <dd>

Handle per la finestra padre.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

Se non si usano i membri dati estesi, è possibile usare la struttura [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md) al posto di **MCI \_ OVLY \_ OPEN \_ PARMS.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 


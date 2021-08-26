---
title: MCI_OVLY_RECT_PARMS struttura (Mciapi.h)
description: La struttura MCI OVLY RECT PARMS contiene informazioni di posizionamento per i \_ \_ comandi \_ MCI PUT e \_ MCI WHERE per i dispositivi di \_ sovrapposizione video.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfd55b2950f6d4268a9af5ee5bdc7fc9c378c4dbaeaa569406339263a2cf85e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039111"
---
# <a name="mci_ovly_rect_parms-structure"></a>Struttura \_ PARMS MCI OVLY \_ RECT \_

La **struttura MCI \_ OVLY \_ RECT \_ PARMS** contiene informazioni di posizionamento per i [**comandi MCI \_ PUT**](mci-put.md) [**e MCI \_ WHERE**](mci-where.md) per i dispositivi di sovrapposizione video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**Rc**
</dt> <dd>

Rettangolo contenente informazioni sul posizionamento. [Le](/previous-versions//ms536136(v=vs.85)) strutture RECT vengono gestite in modo diverso in MCI rispetto ad altre parti Windows; in **MCI, rc.right** contiene la larghezza del rettangolo e **rc.bottom** contiene l'altezza.

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

[**MCI \_ PUT**](mci-put.md)
</dt> <dt>

[**MCI \_ WHERE**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[Rect](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 


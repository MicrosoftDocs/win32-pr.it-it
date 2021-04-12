---
title: Struttura MCI_OVLY_RECT_PARMS (Mciapi. h)
description: La \_ struttura OVLY \_ Rect \_ parametri di MCI contiene informazioni sul posizionamento per i \_ comandi put MCI e MCI \_ Where per i dispositivi con sovrimpressione video.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- Struttura MCI_OVLY_RECT_PARMS di Windows Multimedia
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
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475094"
---
# <a name="mci_ovly_rect_parms-structure"></a>\_ \_ Struttura parametri OVLY Rect di MCI \_

La **struttura \_ OVLY \_ Rect \_ parametri di MCI** contiene informazioni sul posizionamento per i comandi [**\_ put MCI**](mci-put.md) e [**MCI \_ where**](mci-where.md) per i dispositivi con sovrimpressione video.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**RC**
</dt> <dd>

Rettangolo contenente le informazioni sul posizionamento. Le strutture [Rect](/previous-versions//ms536136(v=vs.85)) sono gestite in modo diverso in MCI rispetto ad altre parti di Windows; in MCI, **RC. Right** contiene la larghezza del rettangolo e la versione **RC. Bottom** contiene l'altezza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**\_put MCI**](mci-put.md)
</dt> <dt>

[**MCI \_ dove**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[RECT](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 


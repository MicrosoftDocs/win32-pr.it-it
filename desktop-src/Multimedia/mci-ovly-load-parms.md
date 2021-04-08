---
title: Struttura MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: La \_ struttura OVLY \_ Load \_ parametri di MCI contiene informazioni per il \_ comando di caricamento MCI per i dispositivi con sovrimpressione video.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- Struttura MCI_OVLY_LOAD_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047834"
---
# <a name="mci_ovly_load_parms-structure"></a>\_Struttura OVLY \_ Load \_ parametri di MCI

La **struttura \_ OVLY \_ Load \_ parametri di MCI** contiene informazioni per il comando di [**\_ caricamento MCI**](mci-load.md) per i dispositivi con sovrimpressione video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nome del file da caricare.

</dd> <dt>

**RC**
</dt> <dd>

Identifica l'area del buffer video da aggiornare. Le strutture [Rect](/previous-versions//ms536136(v=vs.85)) sono gestite in modo diverso in MCI rispetto ad altre parti di Windows; in MCI, **RC. Right** contiene la larghezza del rettangolo e la versione **RC. Bottom** contiene l'altezza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**\_carico MCI**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[RECT](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 


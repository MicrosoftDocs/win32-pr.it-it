---
title: Struttura MCI_VD_PLAY_PARMS (Mciapi. h)
description: La \_ struttura MCI VD \_ Play \_ parametri contiene informazioni sulla posizione e sulla velocità del \_ comando MCI Play per i dispositivi videodisco.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- Struttura MCI_VD_PLAY_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048406"
---
# <a name="mci_vd_play_parms-structure"></a>\_Struttura parametri di MCI VD \_ Play \_

La struttura **MCI \_ VD \_ Play \_ parametri** contiene informazioni sulla posizione e sulla velocità del comando [**MCI \_ Play**](mci-play.md) per i dispositivi videodisco.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posizione da cui riprodurre.

</dd> <dt>

**dwTo**
</dt> <dd>

Posizione in cui eseguire la riproduzione.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocità di riproduzione in frame al secondo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

È possibile usare la struttura [**MCI \_ Play \_ parametri**](mci-play-parms.md) anziché **MCI \_ VD \_ Play \_ parametri** se non si usano i membri dati estesi.

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

[**\_riproduzione MCI**](mci-play.md)
</dt> <dt>

[**parametri di MCI \_ Play \_**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 


---
title: MCI_RECORD_PARMS struttura (Mciapi.h)
description: La struttura MCI \_ RECORD \_ PARMS contiene informazioni sul posizionamento per il comando MCI \_ RECORD.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- MCI_RECORD_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c531b5b186a6119a22cafc4e252424ace2e388b2545461b440cd7957694494b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039081"
---
# <a name="mci_record_parms-structure"></a>Struttura MCI \_ RECORD \_ PARMS

La **struttura MCI \_ RECORD \_ PARMS** contiene informazioni sul posizionamento per [**il comando MCI \_ RECORD.**](mci-record.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola più bassa specifica un handle di finestra utilizzato per il flag MCI \_ NOTIFY.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posizione da cui eseguire la riproduzione.

</dd> <dt>

**dwTo**
</dt> <dd>

Posizione in cui eseguire la riproduzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

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

[**MCI \_ RECORD**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 


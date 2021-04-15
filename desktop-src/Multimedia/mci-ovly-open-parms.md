---
title: Struttura MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: La \_ struttura OVLY \_ Open \_ parametri di MCI contiene informazioni per il \_ comando di apertura MCI per i dispositivi con sovrimpressione video.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Struttura MCI_OVLY_OPEN_PARMS di Windows Multimedia
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
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475095"
---
# <a name="mci_ovly_open_parms-structure"></a>\_ \_ Struttura parametri aperta OVLY MCI \_

La **struttura \_ OVLY \_ Open \_ parametri di MCI** contiene informazioni per il comando di [**\_ apertura MCI**](mci-open.md) per i dispositivi con sovrimpressione video.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificatore restituito all'applicazione.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nome o identificatore costante del tipo di dispositivo. Il nome del dispositivo viene in genere ottenuto dal registro di sistema o dal file di SYSTEM.INI. Se questo membro è una costante, può essere uno dei valori elencati nei tipi di [dispositivo MCI](mci-device-types.md).

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nome dell'elemento del dispositivo (in genere un percorso).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias del dispositivo facoltativo.

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

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

Se non si usano i membri dati estesi, è possibile usare la struttura [**\_ \_ parametri Open**](mci-open-parms.md) di MCI al posto di **MCI \_ OVLY \_ Open \_ parametri** .

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

[**\_aperto MCI**](mci-open.md)
</dt> <dt>

[**\_parametri aperto \_ MCI**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 


---
title: Messaggio di EM_SETTARGETDEVICE (RichEdit. h)
description: Imposta il dispositivo di destinazione e lo spessore della riga usati per \ 0034; ciò che viene visualizzato è quello che si ottiene \ 0034; (WYSIWYG) formattazione in un controllo Rich Edit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- Controlli di Windows Message EM_SETTARGETDEVICE
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120127"
---
# <a name="em_settargetdevice-message"></a>\_Messaggio SETTARGETDEVICE em

Imposta il dispositivo di destinazione e la lunghezza di riga usati per la formattazione "What You See is what you get" (WYSIWYG) in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

HDC per il dispositivo di destinazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Spessore riga da usare per la formattazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è zero se l'operazione ha esito negativo o è diverso da zero se ha esito positivo.

## <a name="remarks"></a>Commenti

HDC per la stampante predefinita può essere ottenuto come indicato di seguito.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Se *lParam* è zero, non vengono create interruzioni di riga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 






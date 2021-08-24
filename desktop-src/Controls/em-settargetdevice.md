---
title: EM_SETTARGETDEVICE messaggio (Richedit.h)
description: Imposta il dispositivo di destinazione e lo spessore della linea usati per \ 0034; ciò che viene visualizzato è ciò che si ottiene \ 0034; (WYSIWYG) in un controllo Rich Edit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE di controllo Windows messaggio
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
ms.openlocfilehash: 2d9a3cd4e59f3800b91fedee446e927ab0ec39988474752561a04dace5572ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697591"
---
# <a name="em_settargetdevice-message"></a>Messaggio \_ EM SETTARGETDEVICE

Imposta il dispositivo di destinazione e lo spessore della linea usati per la formattazione "what you see is what you get" (WYSIWYG) in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

HDC per il dispositivo di destinazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Spessore della riga da usare per la formattazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è zero se l'operazione non riesce oppure è diverso da zero se ha esito positivo.

## <a name="remarks"></a>Commenti

L'HDC per la stampante predefinita può essere ottenuto come indicato di seguito.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Se *lParam* è zero, non viene creata alcuna interruzione di riga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 






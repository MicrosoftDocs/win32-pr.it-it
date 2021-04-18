---
description: Il metodo ViewBillboard dell'oggetto UIPreview Visualizza un cartellone creato con il controllo host nella finestra di dialogo attualmente visualizzata.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: UIPreview. ViewBillboard, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327914"
---
# <a name="uipreviewviewbillboard-method"></a>UIPreview. ViewBillboard, metodo

Il metodo **ViewBillboard** dell'oggetto [**UIPreview**](uipreview-object.md) Visualizza un cartellone creato con il controllo host nella finestra di dialogo attualmente visualizzata.

## <a name="syntax"></a>Sintassi


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*control* 
</dt> <dd>

Nome obbligatorio del controllo che ospita il tabellone, con distinzione tra maiuscole e minuscole, con la finestra di dialogo e con le chiavi primarie della tabella del database del controllo.

</dd> <dt>

*Billboard* 
</dt> <dd>

Nome obbligatorio del tabellone da visualizzare utilizzando il controllo specificato e la finestra di dialogo corrente e la chiave primaria della tabella del database Billboard.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





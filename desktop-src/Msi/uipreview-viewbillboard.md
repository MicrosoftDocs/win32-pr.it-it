---
description: Il metodo ViewBillboard dell'oggetto UIPreview visualizza un oggetto creato usando il controllo host nella finestra di dialogo attualmente visualizzata.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Metodo UIPreview.ViewBillboard
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
ms.openlocfilehash: 9892dc68ae5edb66759e4c19499af56d06fb6efac56b823821cd74c4a28644b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810371"
---
# <a name="uipreviewviewbillboard-method"></a>Metodo UIPreview.ViewBillboard

Il **metodo ViewBillboard** dell'oggetto [**UIPreview**](uipreview-object.md) visualizza un oggetto creato usando il controllo host nella finestra di dialogo attualmente visualizzata.

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

Nome obbligatorio del controllo che ospita il pannello, con distinzione tra maiuscole e minuscole, insieme alla finestra di dialogo e alle chiavi primarie della tabella di database Control.

</dd> <dt>

*Billboard* 
</dt> <dd>

Nome obbligatorio del pannello da visualizzare utilizzando il controllo e la finestra di dialogo corrente specificati e la chiave primaria della tabella del database Dei campi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





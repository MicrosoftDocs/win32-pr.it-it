---
title: Proprietà SystemMonitor. BorderStyle
description: Recupera o imposta lo stile del bordo del controllo.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Proprietà BorderStyle SysMon
- Proprietà BorderStyle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873701"
---
# <a name="systemmonitorborderstyle-property"></a>Proprietà SystemMonitor. BorderStyle

Recupera o imposta lo stile del bordo del controllo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a>Valore proprietà

Stile del bordo del controllo.

È possibile impostare questa proprietà su uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                                                                                                   | Significato                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt> </dl>                     | Nessun bordo. Si tratta del valore predefinito.<br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt> </dl> | Fisso, singolo bordo.<br/>                 |



 

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione               | Condizione                                |
|------------------------------|------------------------------------------|
| **System. ArgumentException** | Lo stile del bordo specificato non è valido. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 






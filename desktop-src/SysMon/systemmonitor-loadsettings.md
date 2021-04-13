---
title: SystemMonitor. LoadSettings, metodo
description: Aggiunge i contatori nel file modello HTML al monitor di sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Metodo LoadSettings SysMon
- Metodo LoadSettings SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, Metodo LoadSettings
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400649"
---
# <a name="systemmonitorloadsettings-method"></a>SystemMonitor. LoadSettings, metodo

Aggiunge i contatori nel file modello HTML al monitor di sistema.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SettingsFileName* \[ in\]
</dt> <dd>

Stringa HTML che specifica i contatori da aggiungere al monitor di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per salvare i contatori correnti nel monitor di sistema in un file HTML, chiamare il metodo [**SystemMonitor. SaveAs**](systemmonitor-saveas.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 






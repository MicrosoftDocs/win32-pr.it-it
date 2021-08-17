---
title: Metodo SystemMonitor.LoadSettings
description: Aggiunge i contatori nel file di modello HTML a Monitoraggio di sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Metodo LoadSettings SysMon
- Metodo LoadSettings SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , metodo LoadSettings
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
ms.openlocfilehash: 387bf2e42475d27f5440afb3fa0b945c910b3ac3bad610495936cd3a4a900bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882326"
---
# <a name="systemmonitorloadsettings-method"></a>Metodo SystemMonitor.LoadSettings

Aggiunge i contatori nel file di modello HTML a Monitoraggio di sistema.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SettingsFileName* \[ Pollici\]
</dt> <dd>

Stringa HTML che specifica i contatori da aggiungere a Monitoraggio di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per salvare i contatori correnti in Monitoraggio di sistema in un file HTML, chiamare il [**metodo SystemMonitor.SaveAs.**](systemmonitor-saveas.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 






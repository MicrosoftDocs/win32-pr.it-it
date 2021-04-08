---
description: Imposta la luminosità di visualizzazione di un monitor del computer.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Metodo WmiSetBrightness della classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050233"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Metodo WmiSetBrightness della classe WmiMonitorBrightnessMethods

Il metodo **WmiSetBrightness** imposta la luminosità di visualizzazione di un monitor del computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Timeout* 
</dt> <dd>

Timeout, in secondi.

</dd> <dt>

*Luminosità* 
</dt> <dd>

Luminosità, espressa in percentuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Esempio

Per una descrizione approfondita del recupero e dell'impostazione della luminosità del monitoraggio, vedere l'argomento relativo all' [uso di PowerShell per segnalare e impostare la luminosità](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) del monitoraggio da parte degli Scripting Guy.

Il seguente esempio di PowerShell imposta la luminosità del monitor su 50%.


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 


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
ms.openlocfilehash: 0a9425668ad00422033a77233ade2822966db0f19d6e6628ada24866be9953f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794441"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Metodo WmiSetBrightness della classe WmiMonitorBrightnessMethods

Il **metodo WmiSetBrightness** imposta la luminosità di visualizzazione di un monitor del computer.

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

Luminosità, in percentuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per altre informazioni sui codici di errore, vedere [**Costanti di**](/windows/desktop/WmiSdk/wmi-error-constants) errore WMI o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

## <a name="examples"></a>Esempio

Per una descrizione approfondita del recupero e dell'impostazione della luminosità del monitoraggio, vedere l'argomento del blog Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) (Usare PowerShell per creare report e impostare la luminosità del monitoraggio).

L'esempio di PowerShell seguente imposta la luminosità del monitor sul 50%.


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
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 


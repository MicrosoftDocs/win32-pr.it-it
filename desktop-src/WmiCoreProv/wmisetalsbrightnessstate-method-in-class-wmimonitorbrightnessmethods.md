---
description: Usato per controllare lo stato di luminosità del sensore di luce ambientale.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Metodo WmiSetALSBrightnessState della classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1c8a99ea92391626975d635802f82dd81b663247f4bb3522db19d14237d920f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051119"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a>Metodo WmiSetALSBrightnessState della classe WmiMonitorBrightnessMethods

Il **metodo WmiSetALSBrightnessState** viene usato per controllare lo stato di luminosità del sensore di luce ambientale. Se è stato stabilito un override della luminosità attiva usando il metodo [**WmiSetBrightness,**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) tale override avrà la precedenza sul set di luminosità als usando questo metodo. Per l'attivazione dell'override della luminosità als, è necessario ripristinare i criteri di luminosità usando il metodo [**WmiRevertToPolicyBrightness.**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*State* 
</dt> <dd>

Stato di luminosità als. False disabilita l'override della luminosità als e true lo abilita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per altre informazioni sui codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

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

 


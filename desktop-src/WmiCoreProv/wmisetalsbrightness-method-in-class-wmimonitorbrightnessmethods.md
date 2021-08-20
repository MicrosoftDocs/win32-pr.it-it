---
description: Usato per impostare il valore di luminosità del sensore di luce ambientale.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Metodo WmiSetALSBrightness della classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 93ea1208f81a38b846a1e6a4bf49a8def8a5a8874423a2779b169764016bd193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110755"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Metodo WmiSetALSBrightness della classe WmiMonitorBrightnessMethods

Il **metodo WmiSetALSBrightness** viene usato per impostare il valore di luminosità del sensore di luce ambientale. Se è stato stabilito un override della luminosità attiva tramite il metodo [**WmiSetBrightness,**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) tale override avrà la precedenza sulla luminosità alS impostata usando questo metodo. Per l'applicazione di un override della luminosità alS abilitato, è necessario ripristinare i criteri di luminosità usando il metodo [**WmiRevertToPolicyBrightness.**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Luminosità* 
</dt> <dd>

Luminosità di ALS come percentuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per altre informazioni sui codici di errore, vedere [**Costanti di**](/windows/desktop/WmiSdk/wmi-error-constants) errore WMI o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

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

 


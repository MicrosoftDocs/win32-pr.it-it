---
description: Richiede che il dispositivo acquisisca le informazioni correnti di configurazione, installazione e/o stato in un archivio di backup.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Metodo SaveProperties della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e5910ea87a6321872b009003bf18d26910b53627dba6c51647f2896dde2e686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648163"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>Metodo SaveProperties della classe \_ CIM LogicalDevice

Richiede che il dispositivo acquisisca le informazioni correnti di configurazione, installazione e/o stato in un archivio di backup. L'obiettivo sarebbe quello di usare queste informazioni in un secondo momento (tramite il metodo RestoreProperties), per riportare un dispositivo alla "condizione" corrente. Questo metodo potrebbe non essere supportato da tutti i dispositivi. Il metodo deve restituire 0 in caso di esito positivo, 1 se la richiesta non è supportata e un altro valore se si è verificato un altro errore. In una sottoclasse è possibile specificato il set di codici restituiti possibili, usando un qualificatore ValueMap nel metodo. Le stringhe in cui il contenuto di ValueMap viene 'convertito' possono essere specificate anche nella sottoclasse come qualificatore di matrice Values.

## <a name="syntax"></a>Sintassi


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 





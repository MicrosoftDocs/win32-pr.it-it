---
description: Richiede che il dispositivo acquisisca la configurazione corrente, il programma di installazione e/o le informazioni sullo stato in un archivio di backup.
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
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317768"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>Metodo SaveProperties della classe CIM \_ LogicalDevice

Richiede che il dispositivo acquisisca la configurazione corrente, il programma di installazione e/o le informazioni sullo stato in un archivio di backup. L'obiettivo è quello di usare queste informazioni in un secondo momento (tramite il metodo RestoreProperties), per restituire un dispositivo alla relativa condizione "Condition". Questo metodo potrebbe non essere supportato da tutti i dispositivi. Il metodo deve restituire 0 se ha esito positivo, 1 se la richiesta non è supportata e un altro valore se si sono verificati altri errori. In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore ValueMap nel metodo. Le stringhe a cui è stato convertito il contenuto ValueMap possono anche essere specificate nella sottoclasse come qualificatore della matrice di valori.

## <a name="syntax"></a>Sintassi


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 





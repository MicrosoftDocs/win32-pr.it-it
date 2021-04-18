---
description: Richiede che il dispositivo ristabilisca la configurazione, l'installazione e/o le informazioni sullo stato da un archivio di backup.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Metodo RestoreProperties della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317218"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a>Metodo RestoreProperties della classe CIM \_ LogicalDevice

Richiede che il dispositivo ristabilisca la configurazione, l'installazione e/o le informazioni sullo stato da un archivio di backup. Lo scopo è quello di acquisire queste informazioni in un momento precedente (tramite il metodo SaveProperties) e usarle per restituire un dispositivo a questa "condizione" precedente. Questo metodo potrebbe non essere supportato da tutti i dispositivi. Il metodo deve restituire 0 se ha esito positivo, 1 se la richiesta non è supportata e un altro valore se si sono verificati altri errori. In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore ValueMap nel metodo. Le stringhe a cui è stato convertito il contenuto ValueMap possono anche essere specificate nella sottoclasse come qualificatore della matrice di valori.

## <a name="syntax"></a>Sintassi


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

 

 





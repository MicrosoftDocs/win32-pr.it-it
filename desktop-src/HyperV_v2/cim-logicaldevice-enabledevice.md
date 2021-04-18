---
description: Il metodo EnableDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Metodo EnableDevice della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314364"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>Metodo EnableDevice della classe CIM \_ LogicalDevice

Il metodo EnableDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.

Richiede l'abilitazione di LogicalDevice ("Enabled" parametro di input = TRUE) o disabilitato (= FALSE). In caso di esito positivo, le proprietà StatusInfo/EnabledState del dispositivo devono riflettere lo stato desiderato (abilitato/disabilitato). Si noti che la funzione di questo metodo si sovrappone alla proprietà RequestedState. RequestedState è stato aggiunto al modello per mantenere un record (ovvero un valore permanente) dell'ultima richiesta di stato. Per richiamare il metodo EnableDevice, è necessario impostare la proprietà RequestedState in modo appropriato.

Il codice restituito deve essere 0 se la richiesta è stata eseguita correttamente, 1 se la richiesta non è supportata e un altro valore se si è verificato un errore. In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore ValueMap nel metodo. Le stringhe a cui è stato convertito il contenuto ValueMap possono anche essere specificate nella sottoclasse come qualificatore della matrice di valori.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilitato* \[ in\]
</dt> <dd>

Se TRUE, Abilita il dispositivo, se FALSE Disabilita il dispositivo.

</dd> </dl>

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

 

 





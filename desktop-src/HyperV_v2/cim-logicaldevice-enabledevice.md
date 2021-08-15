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
ms.openlocfilehash: a01d1b206d0d38f74c5701c8c088506792cb6ca6f997b9e0280adcc61e5a8633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648526"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>Metodo EnableDevice della classe \_ CIM LogicalDevice

Il metodo EnableDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.

Richiede che LogicalDevice sia abilitato ("Enabled" parametro di input = TRUE) o disabilitato (= FALSE). In caso di esito positivo, le proprietà StatusInfo/EnabledState del dispositivo devono riflettere lo stato desiderato (abilitato/disabilitato). Si noti che la funzione di questo metodo si sovrappone alla proprietà RequestedState. RequestedState è stato aggiunto al modello per mantenere un record (ad esempio, un valore persistente) dell'ultima richiesta di stato. Richiamare il metodo EnableDevice deve impostare la proprietà RequestedState in modo appropriato.

Il codice restituito deve essere 0 se la richiesta è stata eseguita correttamente, 1 se la richiesta non è supportata e un altro valore se si è verificato un errore. In una sottoclasse è possibile specificato il set di codici restituiti possibili, usando un qualificatore ValueMap nel metodo. Le stringhe in cui il contenuto di ValueMap viene 'convertito' possono essere specificate anche nella sottoclasse come qualificatore di matrice Values.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilitato* \[ Pollici\]
</dt> <dd>

Se TRUE abilita il dispositivo, se FALSE disabilita il dispositivo.

</dd> </dl>

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

 

 





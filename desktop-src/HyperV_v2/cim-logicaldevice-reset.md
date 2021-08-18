---
description: Richiede una reimpostazione di LogicalDevice.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Metodo Reset della classe CIM_LogicalDevice (gestione di Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81f69f57af9d8633874a6b3713ff85cd1342c9df56b22924096619b834f1b867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648536"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a>Metodo Reset della classe CIM_LogicalDevice (gestione di Hyper-V)

Richiede una reimpostazione di LogicalDevice. In una sottoclasse è possibile specificato il set di codici restituiti possibili, usando un qualificatore ValueMap nel metodo. Le stringhe in cui il contenuto di ValueMap viene 'convertito' possono essere specificate anche nella sottoclasse come qualificatore di matrice Values.

## <a name="syntax"></a>Sintassi


```mof
uint32 Reset();
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

 

 





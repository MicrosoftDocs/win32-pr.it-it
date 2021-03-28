---
description: Inserisce l'oggetto utente specificato accanto alla riga per la risoluzione dei nomi.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Metodo DiskQuotaControl. GiveUserNameResolutionPriority (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525332"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>DiskQuotaControl. GiveUserNameResolutionPriority, metodo

Inserisce l'oggetto utente specificato accanto alla riga per la risoluzione dei nomi.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*oUser (valore* 
</dt> <dd>

Tipo: **Object**

Espressione di oggetto che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la risoluzione dei nomi asincrona è abilitata, gli oggetti utente vengono inseriti in una coda. Per impostazione predefinita, vengono serviti nell'ordine in cui vengono inseriti nella coda. Il metodo **GiveUserNameResolutionPriority** sposta un oggetto all'inizio della coda in modo che sia successivo in linea da servire.

Utilizzare la proprietà [**UserNameResolution**](diskquotacontrol-usernameresolution.md) per abilitare la risoluzione dei nomi asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 





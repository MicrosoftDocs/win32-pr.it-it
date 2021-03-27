---
description: IdentityInformationChanged non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'Metodo IIdentityChangeNotify:: IdentityInformationChanged (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881546"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a>Metodo IIdentityChangeNotify:: IdentityInformationChanged

\[**IdentityInformationChanged** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Chiamato quando le informazioni relative a un'identità utente sono state modificate o quando un'identità utente è stata aggiunta o eliminata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwType* 
</dt> <dd>

Tipo: **DWORD**

Valore che specifica il tipo di informazioni modificate o l'operazione eseguita su un'identità. Può essere una combinazione dei valori seguenti.

<dt>



 (IIC \_ \_identità corrente \_ modificata)


</dt> <dd>

L'identità corrente è stata modificata.

</dd> <dt>



 (IIC \_ IDENTITÀ \_ modificata)


</dt> <dd>

Un'identità è stata modificata.

</dd> <dt>



 (IIC \_ IDENTITÀ \_ eliminata)


</dt> <dd>

Un'identità è stata eliminata.

</dd> <dt>



 (IIC \_ IDENTITÀ \_ aggiunta)


</dt> <dd>

È stata aggiunta una nuova identità.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

È possibile implementare questo metodo per fornire un comportamento personalizzato per l'applicazione quando l'elenco di identità utente nel sistema è stato modificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Fine del supporto client<br/>    | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/>    | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



 

 





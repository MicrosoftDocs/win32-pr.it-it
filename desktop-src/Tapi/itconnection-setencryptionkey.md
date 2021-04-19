---
description: Il metodo SetEncryptionKey imposta la chiave di crittografia necessaria per decrittografare la sessione o un'indicazione in un meccanismo per ottenere una chiave utilizzabile per mezzo esterno.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'Metodo ITConnection:: SetEncryptionKey (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326492"
---
# <a name="itconnectionsetencryptionkey-method"></a>Metodo ITConnection:: SetEncryptionKey

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetEncryptionKey** imposta la chiave di crittografia necessaria per decrittografare la sessione o un'indicazione in un meccanismo per ottenere una chiave utilizzabile per mezzo esterno.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pKeyType* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il tipo di chiave di crittografia.

</dd> <dt>

*ppKeyData* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** contenente le informazioni sulla chiave di crittografia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per i parametri *pKeyType* e *ppKeyData* . L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando le variabili non sono più necessarie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 


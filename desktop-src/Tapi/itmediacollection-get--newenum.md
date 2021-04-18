---
description: Il \_ \_ metodo Get NewEnum restituisce un enumeratore per la raccolta.
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'Metodo ITMediaCollection:: get__NewEnum (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfa5655d70026fe2c481aedad0e76923f4caa646
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329733"
---
# <a name="itmediacollectionget__newenum-method"></a>Metodo ITMediaCollection:: Get \_ \_ NewEnum

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ \_ NewEnum** restituisce un enumeratore per la raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out\]
</dt> <dd>

Puntatore a un'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) su un oggetto enumeratore per la raccolta.

Chiamare il metodo [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia **IUnknown** restituita per ottenere un puntatore a un'interfaccia di enumerazione [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) nell'insieme. In **IEnumVARIANT** sono disponibili diversi metodi che è possibile utilizzare per scorrere la raccolta.

Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pval* non è un puntatore valido.<br/>         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Questo metodo è interscambiabile con [**get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) , ad eccezione del fatto che restituisce **IUnknown** invece di [**IEnumMedia**](ienummedia.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 


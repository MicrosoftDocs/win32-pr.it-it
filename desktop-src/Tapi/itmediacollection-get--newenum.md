---
description: 'Metodo ITMediaCollection::get__NewEnum: il metodo get \_ \_ NewEnum restituisce un enumeratore per la raccolta.'
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: Metodo ITMediaCollection::get__NewEnum (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ac5a36324e80e4f2ef3ab49f7e8617aa5d3f5faecb61ca7f8c2de82827354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682681"
---
# <a name="itmediacollectionget__newenum-method"></a>Metodo ITMediaCollection::get \_ \_ NewEnum

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ \_ NewEnum** restituisce un enumeratore per la raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Puntatore a [un'interfaccia IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) su un oggetto enumeratore per la raccolta.

Chiamare il [metodo QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia **IUnknown** restituita per ottenere un puntatore a [un'interfaccia di enumerazione IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) nella raccolta. **IEnumVARIANT** fornisce una serie di metodi che è possibile usare per scorrere la raccolta.

Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pVal* non è un puntatore valido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Questo metodo è intercambiabile con [**get \_ EnumerationIf,**](itmediacollection-get-enumerationif.md) ad eccezione del fatto che restituisce **IUnknown** anziché [**IEnumMedia**](ienummedia.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 


---
title: Metodo CreateObject IWMDRMProvider (wmdrmsdk. h)
description: Il metodo CreateObject recupera un puntatore a un'interfaccia specificata e, se necessario, crea l'oggetto di implementazione.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Metodo CreateObject formato Windows Media
- Metodo CreateObject formato Windows Media, interfaccia IWMDRMProvider
- Interfaccia IWMDRMProvider-formato Windows Media, metodo CreateObject
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325545"
---
# <a name="iwmdrmprovidercreateobject-method"></a>Metodo IWMDRMProvider:: CreateObject

Il metodo **CreateObject** recupera un puntatore a un'interfaccia specificata e, se necessario, crea l'oggetto di implementazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

Identificatore dell'interfaccia da creare. Impostare su uno dei valori seguenti.

-   \_IWMDRMLICENSEMANAGEMENT IID
-   \_IWMDRMLICENSEQUERY IID
-   \_IWMDRMNETRECEIVER IID
-   \_IWMDRMNETTRANSMITTER IID
-   \_IWMDRMSECURITY IID

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo dell'interfaccia richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMProvider**](iwmdrmprovider.md)
</dt> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Interfaccia IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 






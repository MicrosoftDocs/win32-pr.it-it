---
title: Metodo IWMDRMProvider CreateObject (Wmdrmsdk.h)
description: Il metodo CreateObject recupera un puntatore a un'interfaccia specificata, creando l'oggetto di implementazione, se necessario.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Metodo CreateObject windows Media Format
- Metodo CreateObject windows Media Format , interfaccia IWMDRMProvider
- Interfaccia IWMDRMProvider windows Media Format, metodo CreateObject
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
ms.openlocfilehash: f50341e33092b33b19ec3f41d968e0a1b7bc883ae959b200f6c7062e4c69996b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700777"
---
# <a name="iwmdrmprovidercreateobject-method"></a>Metodo IWMDRMProvider::CreateObject

Il **metodo CreateObject** recupera un puntatore a un'interfaccia specificata, creando l'oggetto di implementazione, se necessario.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ Pollici\]
</dt> <dd>

Identificatore dell'interfaccia da creare. Impostare su uno dei valori seguenti.

-   IID \_ IWMDRMLicenseManagement
-   IID \_ IWMDRMLicenseQuery
-   IID \_ IWMDRMNetReceiver
-   IID \_ IWMDRMNetTransmitter
-   IID \_ IWMDRMSecurity

</dd> <dt>

*ppvObject* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo dell'interfaccia richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



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

 

 






---
description: 'Metodo IRTC::D isconnect: il metodo Disconnect disconnette il NPP dalla rete.'
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: Metodo IRTC::D isconnect (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110719"
---
# <a name="irtcdisconnect-method"></a>Metodo IRTC::D isconnect

Il **metodo Disconnect** disconnette il NPP dalla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>      | Il NPP acquisisce i dati. Non è possibile disconnettersi dalla rete mentre è in corso l'acquisizione dei dati.<br/> |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | Il NPP non è connesso alla rete.<br/>                                                                 |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>  | Il NPP è connesso alla rete, ma non con il [metodo IRTC::Connect.](irtc-connect.md)<br/>           |



 

## <a name="remarks"></a>Commenti

Questo metodo non può essere chiamato quando il NPP acquisisce dati. È necessario chiamare il [metodo IRTC::Stop](irtc-stop.md) prima di chiamare IRTC::D isconnect.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 





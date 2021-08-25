---
description: 'Metodo IDelaydC::D isconnect: il metodo Disconnect disconnette il NPP dalla rete.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: Metodo IDelaydC::D isconnect (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ad24ad2557401509c1bc1e076a545f05d1c03dd79fbcf73a05d3efccfdfb8886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910671"
---
# <a name="idelaydcdisconnect-method"></a>Metodo IDelaydC::D isconnect

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



| Codice restituito                                                                                          | Descrizione                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>      | Il NPP acquisisce i dati. Non è possibile disconnettere il NPP dalla rete durante un'acquisizione.<br/>            |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | Il NPP non è connesso alla rete.<br/>                                                               |
| <dl> <dt>**NMERR \_ NON \_ RITARDATO**</dt> </dl>   | Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connessione.](idelaydc-connect.md)<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo non può essere chiamato quando il NPP acquisisce dati. È necessario chiamare il **metodo IDelaydC::Stop** prima di chiamare **Disconnect.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Connessione](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 





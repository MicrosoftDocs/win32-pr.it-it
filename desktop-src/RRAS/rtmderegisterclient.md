---
title: Funzione RtmDeregisterClient (Rtm.h)
description: La funzione RtmDeregisterClient annulla la registrazione del client e libera le risorse associate al client.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- Funzione RtmDeregisterClient RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7df18a4fffa2bdc038aaeb980b76523448e33cca5b7f2e2d558720a5cc9a2c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073861"
---
# <a name="rtmderegisterclient-function"></a>Funzione RtmDeregisterClient

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **funzione RtmDeregisterClient** annulla la registrazione del client e libera le risorse associate al client.

## <a name="syntax"></a>Sintassi


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientHandle* \[ Pollici\]
</dt> <dd>

Handle che identifica il client di cui annullare la registrazione. Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.



| Valore                                                                                                       | Descrizione                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ HANDLE NON \_ VALIDO**</dt> </dl>       | Il *parametro ClientHandle* non è un handle valido.<br/> |
| <dl> <dt>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**</dt> </dl> | Risorse insufficienti per eseguire l'operazione.<br/>  |



 

## <a name="remarks"></a>Commenti

Questa funzione rimuove tutte le route aggiunte dal client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funzioni di Gestione tabelle di routing versione 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 






---
description: Il metodo SetPortInfo imposta il valore della porta a 16 bit per la prima porta e il numero di porte necessarie per una sessione.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'Metodo ITMedia:: SetPortInfo (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332923"
---
# <a name="itmediasetportinfo-method"></a>Metodo ITMedia:: SetPortInfo

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetPortInfo** imposta il valore della porta a 16 bit per la prima porta e il numero di porte necessarie per una sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Presenta* \[ in\]
</dt> <dd>

Porta iniziale. Può trattarsi di un valore compreso nell'intervallo 0-65535.

</dd> <dt>

*NumPorts* \[ in\]
</dt> <dd>

Numero di porte. Può trattarsi di un valore compreso nell'intervallo 0-65535.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *presenta o NumPorts* non è valido.<br/>  |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati. Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> </dl>

 

 





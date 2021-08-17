---
description: Il metodo Create crea un nuovo componente ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: Metodo ITTimeCollection::Create (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65949d0584f6ed41d3e1611c790b6b94dfa88a4e11ba18818974af5d38cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762373"
---
# <a name="ittimecollectioncreate-method"></a>Metodo ITTimeCollection::Create

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo Create** crea un nuovo componente [**ITTime.**](ittime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Indice dell'elemento da creare. La matrice di indici è in base uno.

</dd> <dt>

*ppTime* \[ Cambio\]
</dt> <dd>

Puntatore al componente b creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro ppTime* non è un puntatore valido.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Index* non è valido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

TAPI chiama il **metodo AddRef** sull'interfaccia [**ITTime**](ittime.md) restituita da **ITTimeCollection::Create**. L'applicazione deve **chiamare Release** sull'interfaccia v per liberare le risorse associate.

Questa funzione può inviare dati in modalità non crittografata. Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati. Prima di usare questo metodo, è consigliabile considerare il rischio di sicurezza di inviare i dati in testo non crittografato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 





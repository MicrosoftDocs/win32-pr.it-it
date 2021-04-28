---
description: 'Metodo IEnumMedia::Next: il metodo Next ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: Metodo IEnumMedia::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711e9c844c46aab6ca90988d4e456e926716b201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113439"
---
# <a name="ienummedianext-method"></a>Metodo IEnumMedia::Next

\[ I controlli e le interfacce rendezvous IP Telephony Conferencing non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo Next** ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi richiesti.

</dd> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Puntatore [**all'interfaccia ITMedia.**](itmedia.md)

</dd> <dt>

*pceltFetched* \[ Cambio\]
</dt> <dd>

Puntatore al numero di elementi effettivamente forniti. Può essere **NULL se** *celt* è uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                     | Significato                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo ha restituito il numero di elementi *celt.*<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Il numero di elementi rimanenti è minore di *celt*.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl> | Il *parametro pVal* non è un puntatore valido.<br/>       |



 

## <a name="remarks"></a>Commenti

TAPI chiama il **metodo AddRef** sull'interfaccia [**ITMedia**](itmedia.md) restituita da **IEnumMedia::Next.** L'applicazione deve **chiamare Release** **sull'interfaccia ITMedia** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 





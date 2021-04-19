---
description: Il metodo successivo ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'Metodo IEnumMedia:: Next (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333148"
---
# <a name="ienummedianext-method"></a>IEnumMedia:: Next (metodo)

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **successivo** ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.

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

*celt* \[ in\]
</dt> <dd>

Numero di elementi richiesti.

</dd> <dt>

*pval* \[ out\]
</dt> <dd>

Puntatore all'interfaccia [**ITmedia**](itmedia.md) .

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Puntatore al numero di elementi effettivamente forniti. Può essere **null** se *celt* è uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                     | Significato                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Il metodo ha restituito il numero *celt* di elementi.<br/>         |
| <dl> <dt>**S \_ false**</dt> </dl>   | Il numero di elementi rimanenti è minore di *celt*.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Il parametro *pval* non è un puntatore valido.<br/>       |



 

## <a name="remarks"></a>Commenti

TAPI chiama il metodo **AddRef** sull'interfaccia [**ITmedia**](itmedia.md) restituita da **IEnumMedia:: Next**. L'applicazione deve chiamare **Release** sull'interfaccia **ITmedia** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 





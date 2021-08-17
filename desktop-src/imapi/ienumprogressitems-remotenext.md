---
title: Metodo RemoteNext IEnumProgressItems
description: Supporta un client remoto che vuole recuperare un numero specificato di elementi nella sequenza di enumerazione. | Metodo RemoteNext IEnumProgressItems
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Metodo RemoteNext IMAPI
- Metodo RemoteNext IMAPI, interfaccia IEnumProgressItems
- Interfaccia IEnumProgressItems IMAPI, metodo RemoteNext
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daa2b33fdc356782837aadfe37186bc4cc2b493208fdc78ba645ada9e746582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884851"
---
# <a name="ienumprogressitemsremotenext-method"></a>Metodo IEnumProgressItems::RemoteNext

Supporta un client remoto che vuole recuperare un numero specificato di elementi nella sequenza di enumerazione

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi da recuperare.

</dd> <dt>

*rgelt* \[ Cambio\]
</dt> <dd>

Matrice di [**interfacce IProgressItem.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) Al termine, è necessario rilasciare ogni interfaccia in rgelt.

</dd> <dt>

*pceltFetched* \[ Cambio\]
</dt> <dd>

Numero di elementi restituiti in rgelt. È possibile impostare *pceltFetched* su **NULL** se *celt* è uno. In caso contrario, inizializzare il valore di *pceltFetched* su 0 prima di chiamare questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

S OK viene restituito quando il numero di elementi richiesti ( celt ) viene restituito correttamente o il numero di elementi restituiti \_ (*pceltFetched*) è minore del numero di elementi richiesti.

Altri codici di esito positivo possono essere restituiti come risultato dell'implementazione. I codici di errore seguenti vengono in genere restituiti in caso di errore dell'operazione, ma non rappresentano gli unici valori di errore possibili:



| Codice restituito                                                                                   | Descrizione                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Puntatore non valido.<br/> Valore: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Impossibile allocare la memoria necessaria.<br/> Valore: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o più argomenti non sono validi.<br/> Valore: 0x80070057<br/>    |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | Errore imprevisto.<br/> Valore: 0x8000FFFF<br/>         |



 

## <a name="remarks"></a>Commenti

Se è presente un numero inferiore al numero richiesto di elementi rimanenti nella sequenza, recupera gli elementi rimanenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP2 \[\]<br/>                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Idl<br/>                      | <dl> <dt>Imapi2fs.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumProgressItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[IEnumProgressItems::Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 






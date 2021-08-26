---
description: Il metodo GetChallenge restituisce una richiesta dal smart card.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: Metodo ISCardAuth::GetChallenge
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0132ab8b4b3b2f646639c1618a9f2ca7e67fad1ce2c2fcec38590c7608802091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015421"
---
# <a name="iscardauthgetchallenge-method"></a>Metodo ISCardAuth::GetChallenge

\[Il **metodo GetChallenge** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo GetChallenge** restituisce una richiesta dal [*smart card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lAlgoID* \[ in, facoltativo\]
</dt> <dd>

Algoritmo da utilizzare nel processo di autenticazione.

</dd> <dt>

*lLengthOfChallenge* \[ Pollici\]
</dt> <dd>

Lunghezza massima della risposta prevista.

</dd> <dt>

*pParam* \[ Pollici\]
</dt> <dd>

Oggetto [**IByteBuffer**](ibytebuffer.md) contenente i parametri specifici del fornitore del processo di autenticazione.

</dd> <dt>

*pBuffer* \[ in, out\]
</dt> <dd>

Nell'input punta al buffer.

Nell'output contiene i dati della richiesta dalla scheda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth.**](iscardauth.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> </dl>

 

 

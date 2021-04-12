---
description: Il metodo getchallenge restituisce una richiesta di verifica da parte della smart card.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'Metodo ISCardAuth:: getchallenge'
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
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226603"
---
# <a name="iscardauthgetchallenge-method"></a>Metodo ISCardAuth:: getchallenge

\[Il metodo **getchallenge** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **getchallenge** restituisce una richiesta di verifica da parte della [*Smart Card*](../secgloss/s-gly.md).

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

Algoritmo da usare nel processo di autenticazione.

</dd> <dt>

*lLengthOfChallenge* \[ in\]
</dt> <dd>

Lunghezza massima della risposta prevista.

</dd> <dt>

*pParam* \[ in\]
</dt> <dd>

Oggetto [**IByteBuffer**](ibytebuffer.md) che contiene i parametri specifici del fornitore del processo di autenticazione.

</dd> <dt>

*pbuffer* \[ in uscita\]
</dt> <dd>

In input punta al buffer.

Nell'output, contiene i dati di richiesta della scheda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth**](iscardauth.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> </dl>

 

 

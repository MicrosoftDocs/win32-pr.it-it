---
description: Esegue un'operazione di scrittura e lettura sull'oggetto comando della smart card (unità dati del protocollo dell'applicazione).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'Metodo IsValid:: Transaction (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309436"
---
# <a name="iscardtransaction-method"></a>Metodo IsValid:: Transaction

\[Il metodo di **transazione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo di **transazione** esegue un'operazione di scrittura e lettura nell'oggetto comando della [*Smart Card*](../secgloss/s-gly.md) ([*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md)). La stringa di risposta dalla smart card per la stringa di comando definita nella scheda inviata alla smart card sarà accessibile dopo la restituzione di questa funzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppCmd* \[ in uscita\]
</dt> <dd>

Puntatore all'oggetto comando della smart card.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *ppCmd* non è valido.<br/>           |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppCmd*.<br/>          |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria per soddisfare la richiesta non è disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata l'esecuzione di un'operazione di scrittura e lettura sull'oggetto comando della smart card.


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Scollegare**](iscard-detach.md)
</dt> <dt>

[**Ottieni \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**ottenere \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**ottenere il \_ contesto**](iscard-get-context.md)
</dt> <dt>

[**ottenere il \_ protocollo**](iscard-get-protocol.md)
</dt> <dt>

[**ottenere \_ lo stato**](iscard-get-status.md)
</dt> <dt>

[**Scheda di**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> <dt>

[**Ricollegare**](iscard-reattach.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 

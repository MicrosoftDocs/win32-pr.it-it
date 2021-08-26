---
description: Esegue un'operazione di scrittura e lettura sull'oggetto smart card (application protocol data unit).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: Metodo ISCard::Transaction (Scardmgr.h)
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
ms.openlocfilehash: 60f5be785da0cca6aac4fdf1c098d49548696420042ce60a97a46de73edde9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015561"
---
# <a name="iscardtransaction-method"></a>Metodo ISCard::Transaction

\[Il **metodo** Transaction è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Transaction** esegue un'operazione di scrittura e lettura sull'oggetto [*smart card*](../secgloss/s-gly.md) comando ( unità dati del [*protocollo applicativo).*](../secgloss/a-gly.md) La stringa di risposta smart card per la stringa di comando definita nella scheda inviata al smart card sarà accessibile dopo la fine della funzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Puntatore all'oggetto smart card comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro ppCmd* non è valido.<br/>           |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *ppCmd*.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria per soddisfare la richiesta non è disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata l'esecuzione di un'operazione di scrittura e lettura nell smart card comando.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard è definito come 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**get \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**get \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**Get \_ Context**](iscard-get-context.md)
</dt> <dt>

[**Get \_ Protocol**](iscard-get-protocol.md)
</dt> <dt>

[**get \_ Status**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> <dt>

[**Ricollegare**](iscard-reattach.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 

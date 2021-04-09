---
description: Imposta un nuovo APDU di risposta.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: 'ISCardCmd: metodo:p ut_ApduReply (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879278"
---
# <a name="iscardcmdput_apdureply-method"></a>ISCardCmd::p UT \_ ApduReply metodo

\[Il metodo **put \_ ApduReply** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **put \_ ApduReply** imposta un nuovo [*APDU di risposta*](../secgloss/r-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReplyApdu* \[ in\]
</dt> <dd>

Puntatore al buffer di byte (mappato tramite un oggetto **IStream** ) che contiene il messaggio di riproduzione APDU al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pReplyApdu* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *pReplyApdu*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                            |



 

## <a name="remarks"></a>Commenti

Per ottenere un APDU di risposta esistente, chiamare [**get \_ ApduReply**](iscardcmd-get-apdureply.md).

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare un nuovo [*APDU di risposta*](../secgloss/r-gly.md). Nell'esempio si presuppone che pIByteReply sia un puntatore valido a un'istanza di [**IByteBuffer**](ibytebuffer.md)e che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
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
| Intestazione<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ottenere \_ ApduReply**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**ottenere \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 

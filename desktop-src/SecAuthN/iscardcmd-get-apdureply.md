---
description: Recupera il APDU di risposta, inserendolo in un buffer di byte specifico.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Metodo ISCardCmd:: get_ApduReply (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058316"
---
# <a name="iscardcmdget_apdureply-method"></a>Metodo ISCardCmd:: Get \_ ApduReply

\[Il metodo **get \_ ApduReply** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ ApduReply** Recupera il [*APDU di risposta*](../secgloss/r-gly.md), inserendolo in un buffer di byte specifico. La risposta potrebbe essere **null** se non è stata eseguita alcuna [*transazione*](../secgloss/t-gly.md) sul comando APDU.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppReplyApdu* \[ out\]
</dt> <dd>

Puntatore al buffer di byte (mappato tramite un oggetto **IStream** ) che contiene il messaggio di risposta APDU al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *ppReplyApdu* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppReplyApdu*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                             |



 

## <a name="remarks"></a>Commenti

Per determinare la lunghezza della risposta APDU, chiamare [**get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md).

Per impostare un nuovo APDU di risposta, chiamare [**put \_ ApduReply**](iscardcmd-put-apdureply.md).

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare i dati di risposta. Nell'esempio si presuppone che lLe sia una variabile di tipo **Long** il cui valore è stato impostato da una chiamata precedente al metodo [**ISCardCmd:: Get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) , che pIByteReply è un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) e che pISCardCmd è un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
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

[**ottenere \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Inserisci \_ ApduReply**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 

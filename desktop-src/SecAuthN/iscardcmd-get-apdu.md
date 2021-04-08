---
description: Recupera l'unità dati del protocollo applicazione non elaborata (APDU).
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Metodo ISCardCmd:: get_Apdu (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049506"
---
# <a name="iscardcmdget_apdu-method"></a>Metodo ISCardCmd:: Get \_ APDU

\[Il metodo **get \_ APDU** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ APDU** recupera l' [*unità dati del protocollo applicazione*](../secgloss/a-gly.md) non elaborata (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppApdu* \[ out\]
</dt> <dd>

Puntatore al buffer di byte mappato tramite un oggetto **IStream** che contiene il messaggio APDU al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *ppApdu* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppApdu*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                        |



 

## <a name="remarks"></a>Commenti

Per copiare APDU da un oggetto [**IByteBuffer**](ibytebuffer.md) (**IStream**) in APDU di cui è stato eseguito il wrapper in questo oggetto interfaccia, chiamare [**put \_ APDU**](iscardcmd-put-apdu.md).

Per determinare la lunghezza di APDU, chiamare [**get \_ ApduLength**](iscardcmd-get-apdulength.md).

Per un elenco di tutti i metodi forniti dall'interfaccia [**ISCardCmd**](iscardcmd.md) , vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l' [*unità dati del protocollo applicazione*](../secgloss/a-gly.md) non elaborata (APDU). Nell'esempio si presuppone che pISCardCmd sia un puntatore valido all'interfaccia [**ISCardCmd**](iscardcmd.md) e che pIByteApdu sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
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

[**ottenere \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Inserisci \_ APDU**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 

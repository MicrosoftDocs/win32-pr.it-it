---
description: Copia l'unità APDU (Application Protocol Data Unit) dall'oggetto IByteBuffer (IStream) nell'APDU di cui è stato eseguito il wrapping in questo oggetto di interfaccia.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: Metodo ISCardCmd::p ut_Apdu (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb9b5230564122ac3bed3c34271f0c608924babbbc2c263e10425931fb62337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014615"
---
# <a name="iscardcmdput_apdu-method"></a>Metodo ISCardCmd::p ut \_ Apdu

\[Il **metodo \_ Put Apdu** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo \_ put Apdu** copia l'unità dati del protocollo dell'applicazione (APDU) dall'oggetto [](../secgloss/a-gly.md) [**IByteBuffer**](ibytebuffer.md) (**IStream**) nell'APDU di cui è stato eseguito il wrapping in questo oggetto di interfaccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pApdu* \[ Pollici\]
</dt> <dd>

Puntatore all'APDU ISO 7816-4 in cui copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pApdu* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *pApdu.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                       |



 

## <a name="remarks"></a>Commenti

Per recuperare l'APDU non elaborato dal buffer di byte mappato tramite **un IStream che** contiene il messaggio APDU, chiamare [**get \_ Apdu**](iscardcmd-get-apdu.md).

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd.**](iscardcmd.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore [*smart card*](../secgloss/s-gly.md) se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra come copiare un'APDU da un [**oggetto IByteBuffer**](ibytebuffer.md) (**IStream**) nell'APDU di cui è stato eseguito il wrapping in un oggetto di interfaccia. Nell'esempio si presuppone che pIByteApdu sia un puntatore valido a un'istanza di **IByteBuffer** e che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
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
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**get \_ Apdu**](iscardcmd-get-apdu.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 

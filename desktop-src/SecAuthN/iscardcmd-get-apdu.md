---
description: Recupera l'unità apdu (Application Protocol Data Unit) non elaborata.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: Metodo ISCardCmd::get_Apdu (Scarddat.h)
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
ms.openlocfilehash: 773185563db798877d38d3fb877fe1b4459468e4eeb4d45aed922203bd813418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015091"
---
# <a name="iscardcmdget_apdu-method"></a>Metodo ISCardCmd::get \_ Apdu

\[Il **metodo \_ get Apdu** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo \_ get Apdu** recupera l'unità dati del [*protocollo applicativo*](../secgloss/a-gly.md) (APDU) non elaborata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppApdu* \[ Cambio\]
</dt> <dd>

Puntatore al buffer di byte mappato tramite un **oggetto IStream** che contiene il messaggio APDU al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro ppApdu* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | In ppApdu è stato passato *un puntatore non valido.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                        |



 

## <a name="remarks"></a>Commenti

Per copiare l'APDU da [**un oggetto IByteBuffer**](ibytebuffer.md) (**IStream**) nell'APDU di cui è stato eseguito il wrapping in questo oggetto di interfaccia, chiamare [**put \_ Apdu**](iscardcmd-put-apdu.md).

Per determinare la lunghezza dell'APDU, [**chiamare get \_ ApduLength**](iscardcmd-get-apdulength.md).

Per un elenco di tutti i metodi forniti [**dall'interfaccia ISCardCmd,**](iscardcmd.md) vedere [**ISCardCmd.**](iscardcmd.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore [*smart card*](../secgloss/s-gly.md) se è stata chiamata una funzione smart card per completare la richiesta. Per informazioni sui smart card di errore, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra come recuperare l'unità di dati del protocollo applicativo (APDU, [*Application Protocol Data Unit)*](../secgloss/a-gly.md) non elaborata. L'esempio presuppone che pISCardCmd sia un puntatore valido all'interfaccia [**ISCardCmd**](iscardcmd.md) e che pIByteApdu sia un puntatore valido a un'istanza [**dell'interfaccia IByteBuffer.**](ibytebuffer.md)


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

[**get \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ Apdu**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 

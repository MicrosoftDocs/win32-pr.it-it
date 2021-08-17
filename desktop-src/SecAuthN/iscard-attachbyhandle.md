---
description: Associa l'oggetto ISCard a un handle di smart card aperto e configurato.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: Metodo ISCard::AttachByHandle (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3cf8cf536baab0cef4cd76828ecdf0c594b1fcc7206a73a793c579b9871f242b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482271"
---
# <a name="iscardattachbyhandle-method"></a>Metodo ISCard::AttachByHandle

\[Il **metodo AttachByHandle** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo AttachByHandle** collega l'oggetto [**ISCard**](iscard.md) a un handle di smart card aperto [*e*](../secgloss/s-gly.md) configurato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCard* \[ Pollici\]
</dt> <dd>

Handle a una connessione aperta a un smart card.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata correttamente.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro hCard* non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

Al termine dell'uso dell'handle, rilasciare l'allegato chiamando il metodo [**ISCard::D etach.**](iscard-detach.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la connessione a un handle smart card comando.


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCard è definito come \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**get \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**Ricollegare**](iscard-reattach.md)
</dt> </dl>

 

 

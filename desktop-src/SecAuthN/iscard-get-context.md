---
description: Recupera l'handle di contesto di Resource Manager corrente. Questo metodo restituisce ( \* pContext) == NULL se non è stato stabilito alcun contesto.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: Metodo ISCard::get_Context (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 82094d51912031655585cacde0b156451107276bc08ca1be6dc6d82bdbb3229d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015631"
---
# <a name="iscardget_context-method"></a>Metodo ISCard::get \_ Context

\[Il **metodo get \_ Context** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo get \_ Context** recupera l'handle [*di contesto di Resource Manager*](../secgloss/r-gly.md) corrente. Questo metodo restituisce ( \* *pContext*) == **NULL** se non è stato stabilito alcun contesto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* \[ Cambio\]
</dt> <dd>

Puntatore all'handle di contesto al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata correttamente.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro pContext* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | È stato passato un puntatore non valido in *pContext*.<br/> |



 

## <a name="remarks"></a>Commenti

Il contesto di Resource Manager viene impostato chiamando [*smart card*](../secgloss/s-gly.md) [**funzione SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra il recupero dell'handle [*di contesto di Resource Manager*](../secgloss/r-gly.md) corrente.


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
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

[**get \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**get \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**Get \_ Protocol**](iscard-get-protocol.md)
</dt> <dt>

[**ottenere \_ lo stato**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 

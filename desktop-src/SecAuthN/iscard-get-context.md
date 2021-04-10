---
description: Recupera l'handle di contesto corrente di Resource Manager. Questo metodo restituisce ( \* pContext) = = null se non è stato stabilito alcun contesto.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Metodo IsValid:: get_Context (Scardmgr. h)'
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
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884494"
---
# <a name="iscardget_context-method"></a>Metodo di contesto IsValid:: Get \_

\[Il metodo **get \_ context** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requirements. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ context** recupera l'handle di contesto corrente di [*Resource Manager*](../secgloss/r-gly.md) . Questo metodo restituisce ( \* *pContext*) = = **null** se non è stato stabilito alcun contesto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* \[ out\]
</dt> <dd>

Puntatore all'handle di contesto alla restituzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata correttamente.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *pContext* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Un puntatore errato è stato passato in *pContext*.<br/> |



 

## <a name="remarks"></a>Commenti

Il contesto di Resource Manager viene impostato chiamando la funzione [*Smart Card*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

L'esempio seguente mostra come recuperare l'handle di contesto corrente di [*Resource Manager*](../secgloss/r-gly.md) .


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

[**Ottieni \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**ottenere \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**ottenere il \_ protocollo**](iscard-get-protocol.md)
</dt> <dt>

[**ottenere \_ lo stato**](iscard-get-status.md)
</dt> <dt>

[**Scheda di**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 

---
description: Recupera l'handle per una smart card connessa. Questo metodo restituisce ( \* pHandle) = = null se non è connesso.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'Metodo IsValid:: get_CardHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966455"
---
# <a name="iscardget_cardhandle-method"></a>Metodo IsValid:: Get \_ CardHandle

\[Il metodo **get \_ CardHandle** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ CardHandle** recupera l'handle per una [*Smart Card*](../secgloss/s-gly.md)connessa. Questo metodo restituisce ( \* pHandle) = = **null** se non è connesso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pHandle* \[ out\]
</dt> <dd>

Puntatore all'handle della scheda al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata correttamente.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *pHandle* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Un puntatore errato è stato passato in *pHandle*.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l'handle della smart card.


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
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

[**ottenere il \_ contesto**](iscard-get-context.md)
</dt> <dt>

[**ottenere il \_ protocollo**](iscard-get-protocol.md)
</dt> <dt>

[**ottenere \_ lo stato**](iscard-get-status.md)
</dt> <dt>

[**Scheda di**](iscard.md)
</dt> </dl>

 

 

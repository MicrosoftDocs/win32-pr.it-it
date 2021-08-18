---
description: Rilascia l'accesso esclusivo al smart card.
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: Metodo ISCard::UnlockSCard (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6e61811d84520db2d152fdbfdccfaeefafbee3c0a221e19cf56050096e1f5f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482091"
---
# <a name="iscardunlockscard-method"></a>Metodo ISCard::UnlockSCard

\[Il **metodo UnlockScard** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo UnlockScard** rilascia l'accesso esclusivo [*all'smart card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disposizione* \[ Pollici\]
</dt> <dd>

Indica l'operazione da eseguire con la scheda nel lettore [*connesso.*](../secgloss/r-gly.md)



| Valore                                                                                                                                      | Significato                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**Lasciare**</dt> </dl>       | Lascia il smart card nello stato [*corrente.*](../secgloss/s-gly.md)<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**Reimpostare**</dt> </dl>       | Reimposta l'smart card su uno stato noto.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**UNPOWER**</dt> </dl> | Rimuove l'alimentazione dal smart card.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**Espellere**</dt> </dl>       | Espulse il smart card se il lettore ha funzionalità di espulsione.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro Disposition* non è valido<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra il rilascio dell'accesso esclusivo al smart card.


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
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

[**ISCard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> </dl>

 

 

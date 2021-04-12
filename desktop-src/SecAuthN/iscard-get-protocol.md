---
description: Recupera l'identificatore del protocollo attualmente in uso nella smart card.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'Metodo IsValid:: get_Protocol (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348051"
---
# <a name="iscardget_protocol-method"></a>Metodo IsValid:: Get \_ Protocol

\[Il metodo **get \_ Protocol** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ Protocol** recupera l'identificatore del protocollo attualmente in uso nella [*Smart Card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProtocol* \[ out\]
</dt> <dd>

Puntatore all'identificatore del protocollo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *pProtocol* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Un puntatore errato è stato passato in *pProtocol*.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l'identificatore del protocollo attualmente in uso nella smart card.


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
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

[**ottenere il \_ contesto**](iscard-get-context.md)
</dt> <dt>

[**ottenere \_ lo stato**](iscard-get-status.md)
</dt> <dt>

[**Scheda di**](iscard.md)
</dt> </dl>

 

 

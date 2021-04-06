---
description: Determina la lunghezza, in byte, dell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: 'Metodo ISCardCmd:: get_ApduLength (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1535d2b4b67861b42719506ebd48cca4c49d5c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760115"
---
# <a name="iscardcmdget_apdulength-method"></a>Metodo ISCardCmd:: Get \_ ApduLength

\[Il metodo **get \_ ApduLength** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ ApduLength** determina la lunghezza, in byte, dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plSize* \[ out\]
</dt> <dd>

Puntatore alla lunghezza di APDU.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *plSize* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *plSize*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                        |



 

## <a name="remarks"></a>Commenti

Per recuperare l' [*unità dati del protocollo applicazione*](../secgloss/a-gly.md) (APDU) non elaborata dal buffer di byte mappato tramite un **IStream** che contiene il messaggio APDU, chiamare [**get \_ APDU**](iscardcmd-get-apdu.md).

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare la lunghezza dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU). Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
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

[**ottenere \_ APDU**](iscardcmd-get-apdu.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 

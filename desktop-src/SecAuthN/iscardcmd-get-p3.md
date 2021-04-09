---
description: Recupera il terzo parametro (P3) byte dall'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Metodo ISCardCmd:: get_P3 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129339"
---
# <a name="iscardcmdget_p3-method"></a>Metodo ISCardCmd:: Get \_ P3

\[Il metodo **get \_ P3** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ P3** Recupera il terzo parametro (P3) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU). Questo valore di byte di sola lettura rappresenta le dimensioni della parte di dati di APDU.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyP3* \[ out\]
</dt> <dd>

Puntatore al byte che rappresenta il P3 da APDU al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PbyP3* non valido.<br/>            |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *pbyP3*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                       |



 

## <a name="remarks"></a>Commenti

Il parametro P3 è di sola lettura e pertanto non può essere impostato.

Per ottenere i parametri P1 o P2, chiamare rispettivamente [**get \_ P1**](iscardcmd-get-p1.md) e [**get \_ P2**](iscardcmd-get-p2.md) .

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare il terzo parametro (P3) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU). Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
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

[**ottenere \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**ottenere \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 

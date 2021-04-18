---
description: Imposta il primo parametro (P1) byte dell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: 'ISCardCmd: metodo:p ut_P1 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314738"
---
# <a name="iscardcmdput_p1-method"></a>ISCardCmd::p UT \_ P1 (metodo)

\[Il metodo **put \_ P1** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **put \_ P1** imposta il primo parametro (P1) byte dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP1* \[ in\]
</dt> <dd>

Byte che rappresenta il campo P1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *byP1* non è valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                     |



 

## <a name="remarks"></a>Commenti

Per impostare il valore P2 di APDU, chiamare [**get \_ p2**](iscardcmd-get-p2.md).

Per recuperare i valori P1, P2 e P3 esistenti, chiamare [**get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) o [**get \_ P3**](iscardcmd-get-p3.md) rispettivamente.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare il primo parametro (P1) byte dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU). Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
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

[**ottenere \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Inserisci \_ P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 

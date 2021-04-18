---
description: Specifica un nuovo identificatore di classe alternativo nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: 'ISCardCmd: metodo:p ut_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307237"
---
# <a name="iscardcmdput_alternateclassid-method"></a>ISCardCmd::p UT \_ AlternateClassId metodo

\[Il metodo **put \_ AlternateClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **put \_ AlternateClassId** specifica un nuovo identificatore di classe alternativo nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byClass* \[ in\]
</dt> <dd>

Identificatore di classe alternativo. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata correttamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *byClass* non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

Con le comunicazioni che usano il [*protocollo T = 0*](../secgloss/t-gly.md), i comandi della scheda aggiuntivi possono essere generati automaticamente da APDU e inviati all'unità dati del protocollo di trasmissione (TPDU). I comandi aggiuntivi usano in genere lo stesso ID di classe del comando originale. la specifica di un nuovo ID di classe per mezzo di questo metodo consente ai comandi generati automaticamente di usare il nuovo ID di classe.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare un nuovo identificatore di classe alternativo nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU). Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
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

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**ottenere \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 

---
description: Recupera il valore dell'ID della classe alternativa.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Metodo ISCardCmd:: get_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317063"
---
# <a name="iscardcmdget_alternateclassid-method"></a>Metodo ISCardCmd:: Get \_ AlternateClassId

\[Il metodo **get \_ AlternateClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ AlternateClassId** Recupera il valore dell'ID di classe alternativo. Questo metodo avrà esito negativo a meno che l'ID alternativo non sia stato impostato da una chiamata precedente a [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyClass* \[ out\]
</dt> <dd>

Puntatore al byte che contiene il valore dell'ID di classe alternativo al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce i valori possibili seguenti.



| Codice restituito                                                                                    | Descrizione                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>           | Operazione completata correttamente.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il parametro *pbyClass* non è valido.<br/>                                                                                           |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl> | L'ID di classe alternativo non è stato impostato in precedenza da una chiamata a [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo si applica alle comunicazioni che utilizzano il [*protocollo T = 0*](../secgloss/t-gly.md). Per altre informazioni, vedere [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l'ID della classe alternativa. Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
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

[**Inserisci \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 

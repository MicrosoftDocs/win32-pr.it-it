---
description: Recupera il valore dell'ID di classe alternativo.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: Metodo ISCardCmd::get_AlternateClassId (Scarddat.h)
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
ms.openlocfilehash: ac6d74f89eaf2c42ec9fc00cef9d82735b4b28885180c3c5d429dad7450e3c74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577781"
---
# <a name="iscardcmdget_alternateclassid-method"></a>Metodo ISCardCmd::get \_ AlternateClassId

\[Il **metodo get \_ AlternateClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo get \_ AlternateClassId** recupera il valore dell'ID di classe alternativo. Questo metodo avrà esito negativo a meno che l'ID alternativo non sia stato impostato da una chiamata precedente per [**inserire \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyClass* \[ Cambio\]
</dt> <dd>

Puntatore al byte che contiene il valore ID di classe alternativo al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce i valori possibili seguenti.



| Codice restituito                                                                                    | Descrizione                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è stata completata correttamente.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il *parametro pbyClass* non è valido.<br/>                                                                                           |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | L'ID di classe alternativo non è stato impostato in precedenza da una chiamata a [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo si applica alle comunicazioni che usano [*il protocollo T=0.*](../secgloss/t-gly.md) Per altre informazioni, vedere [**put \_ AlternateClassId.**](iscardcmd-put-alternateclassid.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l'ID di classe alternativo. Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 

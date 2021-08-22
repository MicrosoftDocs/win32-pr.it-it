---
description: Specifica un nuovo identificatore di classe alternativo nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: Metodo ISCardCmd::p ut_AlternateClassId (Scarddat.h)
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
ms.openlocfilehash: fd1f74dee017cb72a67ecb4a9fc42da85153966336b25e54819be13464b3b7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481561"
---
# <a name="iscardcmdput_alternateclassid-method"></a>Metodo ISCardCmd::p ut \_ AlternateClassId

\[Il **metodo \_ put AlternateClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo put \_ AlternateClassId** specifica un nuovo identificatore di classe alternativo nell'unità dati del protocollo [*dell'applicazione*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byClass* \[ Pollici\]
</dt> <dd>

Identificatore di classe alternativo. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata correttamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro byClass* non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

Con le comunicazioni che usano il protocollo [*T=0,*](../secgloss/t-gly.md)è possibile generare automaticamente comandi aggiuntivi per le schede tramite APDU e inviare all'unità dati del protocollo di trasmissione (TPDU). I comandi aggiuntivi usano in genere lo stesso ID classe del comando originale. Se si specifica un nuovo ID classe tramite questo metodo, i comandi generati automaticamente possono usare il nuovo ID classe.

## <a name="examples"></a>Esempio

L'esempio seguente illustra come impostare un nuovo identificatore di classe alternativo nell'unità dati del protocollo [*dell'applicazione*](../secgloss/a-gly.md) (APDU). L'esempio presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd è definito come \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**get \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 

---
description: Imposta il campo dati nell'unità dati del protocollo applicativo (APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: Metodo ISCardCmd::p ut_Data (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 53b32cd585e87af2884920305b8aa0ae427fa9389e3c528243c18fb548289a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481431"
---
# <a name="iscardcmdput_data-method"></a>Metodo ISCardCmd::p ut \_ Data

\[Il **metodo put \_ Data** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo put \_ Data** imposta il campo dati nell'unità dati [*del protocollo applicativo*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore all'oggetto buffer di byte (**IStream**) da copiare nel campo dati APDU.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pData* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *pData.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                       |



 

## <a name="remarks"></a>Commenti

Quando si imposta una nuova parte di dati del messaggio, la lunghezza del campo dati viene calcolata e archiviata nel parametro P3 dell'APDU. Per recuperare la lunghezza del campo dati, chiamare [**il metodo \_ get P3.**](iscardcmd-get-p3.md)

Per recuperare il campo dati dall'APDU, chiamare [**get \_ Data**](iscardcmd-get-data.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra come impostare il campo dati nell'unità dati [*del protocollo applicativo*](../secgloss/a-gly.md) (APDU). L'esempio presuppone che pIByteData sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) e che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
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

[**Ottenere \_ i dati**](iscardcmd-get-data.md)
</dt> <dt>

[**get \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 

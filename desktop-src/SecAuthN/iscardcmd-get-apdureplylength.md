---
description: Determina la lunghezza (in byte) dell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: Metodo ISCardCmd::get_ApduReplyLength (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bb08be6ad4e916a6dc7b1521dee7aac2dcac55c2bd0ac541278c9e00e34b6ed0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577691"
---
# <a name="iscardcmdget_apdureplylength-method"></a>Metodo ISCardCmd::get \_ ApduReplyLength

\[Il **metodo \_ get ApduReplyLength** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo get \_ ApduReplyLength** determina la lunghezza (in byte) dell'unità dati del protocollo [*applicativo*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plSize* \[ Cambio\]
</dt> <dd>

Puntatore alla dimensione del messaggio APDU di risposta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro plSize* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *plSize.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                        |



 

## <a name="remarks"></a>Commenti

Per ottenere un'APDU di risposta esistente, [**chiamare get \_ ApduReply**](iscardcmd-get-apdureply.md).

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd.**](iscardcmd.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

L'esempio seguente mostra come recuperare la lunghezza [*dell'APDU di risposta*](../secgloss/r-gly.md). Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
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

[**get \_ ApduReply**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ ApduReply**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 

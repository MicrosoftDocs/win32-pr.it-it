---
description: Recupera il secondo byte del parametro (P2) dall'unità APDU (Application Protocol Data Unit).
ms.assetid: c719786f-0f50-472e-a92e-a64c333fc255
title: Metodo ISCardCmd::get_P2 (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf9d5735e4583e0b55a91e6c45f9f23905bd199e15697596a93b06c2347aab65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577551"
---
# <a name="iscardcmdget_p2-method"></a>Metodo ISCardCmd::get \_ P2

\[Il **metodo get \_ P2** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo get \_ P2** recupera il secondo byte del parametro (P2) dall'unità APDU [*(Application Protocol Data Unit).*](../secgloss/a-gly.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_P2(
  [out] BYTE *pbyP2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyP2* \[ Cambio\]
</dt> <dd>

Puntatore al byte che rappresenta il P2 dall'APDU al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pbyP2* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *pbyP2.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                       |



 

## <a name="remarks"></a>Commenti

Per impostare il parametro P2 su un nuovo valore, chiamare [**put \_ P2**](iscardcmd-put-p2.md).

Per ottenere i parametri P1 o P3, chiamare [**rispettivamente get \_ P1**](iscardcmd-get-p1.md) [**e get \_ P3.**](iscardcmd-get-p3.md)

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd.**](iscardcmd.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore [*smart card*](../secgloss/s-gly.md) se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra come recuperare il secondo byte del parametro (P2) dall'unità APDU [*(Application Protocol Data Unit).*](../secgloss/a-gly.md) Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


```C++
BYTE  byP2;
HRESULT  hr;

// Retrieve the P2 byte.
hr = pISCardCmd->get_P2(&byP2);
if (FAILED(hr))
{
  printf("Failed get_P2\n");
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

[**get \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**get \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 

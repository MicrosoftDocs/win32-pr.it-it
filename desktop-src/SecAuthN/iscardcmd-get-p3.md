---
description: Recupera il terzo byte del parametro (P3) dall'unità apdu (Application Protocol Data Unit).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: Metodo ISCardCmd::get_P3 (Scarddat.h)
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
ms.openlocfilehash: 4ebf19856126d65824b9214973aa90412475afeecf707a17f9b9434d9852945f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014921"
---
# <a name="iscardcmdget_p3-method"></a>Metodo ISCardCmd::get \_ P3

\[Il **metodo \_ get P3** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo get \_ P3** recupera il terzo byte del parametro (P3) dall'unità APDU [*(Application Protocol Data Unit).*](../secgloss/a-gly.md) Questo valore di byte di sola lettura rappresenta le dimensioni della parte di dati dell'APDU.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyP3* \[ Cambio\]
</dt> <dd>

Puntatore al byte che rappresenta il P3 dall'APDU al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PbyP3* non è valido.<br/>            |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *pbyP3.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                       |



 

## <a name="remarks"></a>Commenti

Il parametro P3 è di sola lettura e pertanto non può essere impostato.

Per ottenere i parametri P1 o P2, chiamare [**rispettivamente get \_ P1**](iscardcmd-get-p1.md) [**e get \_ P2.**](iscardcmd-get-p2.md)

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd.**](iscardcmd.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore [*smart card*](../secgloss/s-gly.md) se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra come recuperare il terzo byte del parametro (P3) dall'unità apdu [*(Application Protocol Data Unit).*](../secgloss/a-gly.md) Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


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

[**get \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 

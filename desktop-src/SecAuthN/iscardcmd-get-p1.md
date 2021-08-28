---
description: Recupera il primo byte del parametro (P1) dall'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: Metodo ISCardCmd::get_P1 (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 94fd7dbe7629ebc3137a6323515d401688dc489cf08c7bb3e6d4262527d4d0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014961"
---
# <a name="iscardcmdget_p1-method"></a>Metodo ISCardCmd::get \_ P1

\[Il **metodo \_ get P1** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo get \_ P1** recupera il primo byte del parametro (P1) dall'unità dati del protocollo [*dell'applicazione*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyP1* \[ Cambio\]
</dt> <dd>

Puntatore al byte P1 nella APDU in caso di restituzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pbyP1* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido in *pbyP1.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                       |



 

## <a name="remarks"></a>Commenti

Per impostare il parametro P1 su un nuovo valore, chiamare [**put \_ P1**](iscardcmd-put-p1.md).

Per ottenere i parametri P2 o P3, chiamare [**rispettivamente get \_ P2**](iscardcmd-get-p2.md) e [**get \_ P3.**](iscardcmd-get-p3.md)

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati [](../secgloss/s-gly.md) in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra come recuperare il primo byte del parametro (P1) dall'unità dati del protocollo [*dell'applicazione*](../secgloss/a-gly.md) (APDU). L'esempio presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
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

[**ottenere \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**ottenere \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 

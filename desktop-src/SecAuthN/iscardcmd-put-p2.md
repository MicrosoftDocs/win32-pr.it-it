---
description: Imposta il secondo byte del parametro (P2) nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: Metodo ISCardCmd::p ut_P2 (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a66ef756d65e4cc011e6a5e4797a8ccae690dd404b6f25f1f9a7d3bbb2826069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014581"
---
# <a name="iscardcmdput_p2-method"></a>Metodo ISCardCmd::p ut \_ P2

\[Il **metodo \_ put P2** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo put \_ P2** imposta il secondo byte del parametro (P2) nell'unità dati del protocollo [*dell'applicazione*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP2* \[ Pollici\]
</dt> <dd>

Byte che rappresenta il campo P2.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro byP2* non è valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                     |



 

## <a name="remarks"></a>Commenti

Per impostare il valore P1 dell'APDU, chiamare [**put \_ P1**](iscardcmd-put-p1.md).

Per recuperare i valori P1, P2 e P3 esistenti, chiamare [**rispettivamente get \_ P1,**](iscardcmd-get-p1.md) [**get \_ P2**](iscardcmd-get-p2.md) o [**\_ P3.**](iscardcmd-get-p3.md)

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).

Oltre ai codici di errore COM elencati [](../secgloss/s-gly.md) in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra come impostare il secondo byte del parametro (P2) dell'unità dati del protocollo [*dell'applicazione*](../secgloss/a-gly.md) (APDU). L'esempio presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
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

[**ottenere \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**ottenere \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**ottenere \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 

---
description: Crea e aggiunge una nuova condivisione DDE alla gestione del database di condivisione DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Funzione NDdeShareAdd (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316917"
---
# <a name="nddeshareadd-function"></a>NDdeShareAdd (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Crea e aggiunge una nuova condivisione DDE alla gestione del database di condivisione DDE (DSDM).

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Nome del server di cui è necessario modificare il DSDM.

</dd> <dt>

*nLevel* \[ in\]
</dt> <dd>

Livello di informazioni. Questo parametro deve essere 2.

</dd> <dt>

*PSD* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) da associare a questa condivisione e in base a cui verranno eseguiti i controlli di accesso per i successivi avvii a questa condivisione. Questo parametro può essere **null**, nel qual caso DSDM crea un descrittore di sicurezza predefinito che concede al proprietario il "controllo completo" e "Read and link" a tutti.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Puntatore alla struttura [**NDDESHAREINFO**](nddeshareinfo-str.md) che definisce l'elenco ApplicationTopic associato alla condivisione DDE creata e ad altri parametri. Questo parametro non può essere **null**.

</dd> <dt>

*cBufSize* \[ in\]
</dt> <dd>

Dimensioni in byte della struttura *lpBuffer* . Questo parametro non può essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Commenti

Prima che un client possa connettersi alla condivisione DDE, deve essere considerato attendibile con [**NDdeSetTrustedShare**](nddesettrustedshare.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeShareAddW** (Unicode) e **NDdeShareAddA** (ANSI)<br/>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 


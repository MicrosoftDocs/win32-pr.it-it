---
description: Recupera il descrittore di sicurezza associato alla condivisione DDE. Questa operazione viene eseguita in genere per la modifica.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Funzione NDdeGetShareSecurity (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884997"
---
# <a name="nddegetsharesecurity-function"></a>NDdeGetShareSecurity (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Recupera il descrittore di sicurezza associato alla condivisione DDE. Questa operazione viene eseguita in genere per la modifica.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Nome del server in cui risiede l'DSDM.

</dd> <dt>

*lpszShareName* \[ in\]
</dt> <dd>

Nome della condivisione il cui descrittore di sicurezza deve essere recuperato da DSDM. Questo parametro non può essere **null**.

</dd> <dt>

*si* \[ in\]
</dt> <dd>

Valore [**delle \_ informazioni di sicurezza**](/windows/desktop/SecAuthZ/security-information) che specifica le informazioni di sicurezza da recuperare dal descrittore di sicurezza associato alla condivisione.

</dd> <dt>

*PSD* \[ out\]
</dt> <dd>

Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che riceve il descrittore di sicurezza relativo. Questo parametro può essere **NULL**. Se questo parametro è **null**, DSDM determina la dimensione delle informazioni di sicurezza richieste e restituisce il numero di byte necessari nel parametro *lpcbsdRequired* insieme al codice di errore NDDE \_ BUF \_ troppo \_ piccolo.

</dd> <dt>

*cbSD* \[ in\]
</dt> <dd>

Dimensioni del buffer *PSD* . Se *PSD* è **null**, questo parametro deve essere zero.

</dd> <dt>

*lpcbsdRequired* \[ out\]
</dt> <dd>

Puntatore alla variabile che riceve le dimensioni effettive del descrittore di sicurezza recuperato. Questo parametro non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md). Se il parametro *PSD* è **null**, restituisce NDDE \_ BUF \_ troppo \_ piccolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeGetShareSecurityW** (Unicode) e **NDdeGetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**informazioni di sicurezza \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 


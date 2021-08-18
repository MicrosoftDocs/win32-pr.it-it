---
description: Recupera il descrittore di sicurezza associato alla condivisione DDE. Questa operazione viene in genere eseguita per la modifica.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Funzione NDdeGetShareSecurity (Nddeapi.h)
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
ms.openlocfilehash: 101767516e8bd726ebf1a64ad83cfd924b3696a56d810895b4d9a9ed9a1e0ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829341"
---
# <a name="nddegetsharesecurity-function"></a>Funzione NDdeGetShareSecurity

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera il descrittore di sicurezza associato alla condivisione DDE. Questa operazione viene in genere eseguita per la modifica.

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

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server in cui risiede DSDM.

</dd> <dt>

*lpszShareName* \[ Pollici\]
</dt> <dd>

Nome della condivisione il cui descrittore di sicurezza deve essere recuperato da DSDM. Questo parametro non può essere **NULL.**

</dd> <dt>

*si* \[ Pollici\]
</dt> <dd>

Valore [**SECURITY \_ INFORMATION**](/windows/desktop/SecAuthZ/security-information) che specifica le informazioni di sicurezza da recuperare dal descrittore di sicurezza associato alla condivisione.

</dd> <dt>

*pSD* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che riceve il descrittore di sicurezza self-relative. Questo parametro può essere **NULL**. Se questo parametro è **NULL,** DSDM determina le dimensioni delle informazioni di sicurezza richieste e restituisce il numero di byte necessari nel parametro *lpcbsdRequired* insieme al codice di errore NDDE \_ BUF \_ TOO \_ SMALL.

</dd> <dt>

*cbSD* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *pSD.* Questo parametro deve essere zero se *pSD* è **NULL.**

</dd> <dt>

*lpcbsdRequired* \[ Cambio\]
</dt> <dd>

Puntatore alla variabile che riceve le dimensioni effettive del descrittore di sicurezza recuperato. Questo parametro non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md). Se il *parametro pSD* è **NULL,** restituisce NDDE \_ BUF \_ TOO \_ SMALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeGetShareSecurityW** (Unicode) e **NDdeGetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**INFORMAZIONI SULLA \_ SICUREZZA**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 


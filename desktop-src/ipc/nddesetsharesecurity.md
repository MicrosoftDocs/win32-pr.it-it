---
description: Imposta il descrittore di sicurezza associato alla condivisione DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Funzione NDdeSetShareSecurity (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 00e6d8c4b235e8f7d02ba22e737fc4de9bf4a739864afb1464e6f84c620faa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481825"
---
# <a name="nddesetsharesecurity-function"></a>Funzione NDdeSetShareSecurity

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Imposta il descrittore di sicurezza associato alla condivisione DDE. Questa operazione viene eseguita in genere dopo la modifica dell'elenco DACL assegnato alla condivisione DDE.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server il cui DSDM deve essere modificato.

</dd> <dt>

*lpszShareName* \[ Pollici\]
</dt> <dd>

Nome della condivisione il cui descrittore di sicurezza deve essere modificato. Questo parametro non può essere **NULL.**

</dd> <dt>

*si* \[ Pollici\]
</dt> <dd>

Valore [**SECURITY \_ INFORMATION**](/windows/desktop/SecAuthZ/security-information) che identifica le informazioni di sicurezza da recuperare.

</dd> <dt>

*pSD* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che contiene informazioni di sicurezza. Questo parametro non può essere **NULL** e deve puntare a un descrittore di sicurezza valido.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Commenti

Per modificare [**il \_ DESCRITTORE DI SICUREZZA**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associato a una condivisione DDE in DSDM, l'utente deve disporre dei privilegi appropriati. L'autore della condivisione dispone di questo privilegio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeSetShareSecurityW** (Unicode) e **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**INFORMAZIONI SULLA \_ SICUREZZA**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 


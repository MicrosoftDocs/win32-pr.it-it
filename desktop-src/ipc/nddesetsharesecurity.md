---
description: Imposta il descrittore di sicurezza associato alla condivisione DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Funzione NDdeSetShareSecurity (nddeapi. h)
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
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315053"
---
# <a name="nddesetsharesecurity-function"></a>NDdeSetShareSecurity (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Imposta il descrittore di sicurezza associato alla condivisione DDE. Questa operazione viene eseguita in genere dopo la modifica del DACL assegnato alla condivisione DDE.

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

*lpszServer* \[ in\]
</dt> <dd>

Nome del server di cui è necessario modificare il DSDM.

</dd> <dt>

*lpszShareName* \[ in\]
</dt> <dd>

Nome della condivisione di cui è necessario modificare il descrittore di sicurezza. Questo parametro non può essere **null**.

</dd> <dt>

*si* \[ in\]
</dt> <dd>

Valore [**delle \_ informazioni di sicurezza**](/windows/desktop/SecAuthZ/security-information) che identifica le informazioni di sicurezza da recuperare.

</dd> <dt>

*PSD* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che contiene informazioni sulla sicurezza. Questo parametro non può essere **null** e deve puntare a un descrittore di sicurezza valido.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Commenti

Per modificare il [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associato a una condivisione DDE in DSDM, l'utente deve disporre dei privilegi appropriati. l'autore della condivisione dispone di questo privilegio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeSetShareSecurityW** (Unicode) e **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**informazioni di sicurezza \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 


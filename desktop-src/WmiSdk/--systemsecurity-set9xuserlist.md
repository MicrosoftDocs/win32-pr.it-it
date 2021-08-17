---
description: Imposta i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo di accesso tramite Windows descrittori di sicurezza non è disponibile.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: __SystemSecurity::Set9XUserList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: d1185fa91d9d12e240f592d458b975b650947cf5b8cd1b289a7e016b455556a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109962"
---
# <a name="__systemsecurityset9xuserlist-method"></a>\_\_Metodo SystemSecurity::Set9XUserList

Il **\_ \_ metodo SystemSecurity::Set9XUserList** imposta i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo di accesso tramite descrittori di sicurezza Windows non è disponibile.

L'elenco viene specificato come matrice di oggetti incorporati in cui ogni oggetto è un'istanza della [**\_ \_ classe NTLMUser9X.**](--ntlmuser9x.md) Questa funzione è simile al descrittore di sicurezza, ma è più limitata. I gruppi non sono supportati e non è disponibile alcun controllo sull'accesso locale, perché l'utente locale ha sempre accesso completo. Sono consentite sia le voci di controllo di accesso (ACE) che le voci di controllo di accesso consentite e, per questo, l'ordine ACE è importante nell'elenco di controllo di accesso discrezionale (DACL). Per altre informazioni, vedere [Order of AEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ul* \[ Pollici\]
</dt> <dd>

Matrice di utenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **HRESULT** che indica lo stato della chiamata al metodo. Nell'elenco seguente sono elencati i valori restituiti significativi per **Set9XUserList**. Per script e Visual Basic applicazioni, il risultato può essere ottenuto da [OutParameters.ReturnValue](parsing-outparameters-objects.md). Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**METODO \_ WBEM E \_ \_ DISABILITATO**
</dt> <dd>

Questo metodo non è supportato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::SetSD**](--systemsecurity-setsd.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Descrittore di sicurezza Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> </dl>

 


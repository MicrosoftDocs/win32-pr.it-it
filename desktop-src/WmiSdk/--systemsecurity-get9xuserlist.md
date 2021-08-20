---
description: Ottiene i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows , in cui il controllo di accesso Windows descrittori di sicurezza non è disponibile.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: __SystemSecurity::Get9XUserList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: cfb6f0b9bb503e212e00d5343b55d6a9e20fbc8acfb0a5b534e8848cc6d3d931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110104"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_Metodo SystemSecurity::Get9XUserList

Il [**\_ \_ metodo SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) ottiene i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows , in cui il controllo di accesso tramite descrittori di sicurezza di Windows non è disponibile.

Questa funzione è simile al descrittore di sicurezza, ma è più limitata. I gruppi non sono supportati e non è disponibile alcun controllo sull'accesso locale, perché l'utente locale ha sempre l'accesso completo. Sono consentite sia le voci di controllo di accesso negate che consentite e, per questo, l'ordine ACE è importante nell'elenco di controllo di accesso discrezionale (DACL). Per altre informazioni, vedere [Ordine delle ACE in un dacl.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ul* \[ Cambio\]
</dt> <dd>

Matrice di utenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **HRESULT** che indica lo stato della chiamata al metodo. Nell'elenco seguente sono elencati i valori restituiti significativi per **Get9XUserList**. Per script e Visual Basic applicazioni, il risultato può essere [OutParameters.ReturnValue](parsing-outparameters-objects.md). Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

<dl> <dt>

**METODO WBEM \_ E \_ \_ DISABILITATO**
</dt> <dd>

Questo metodo non è supportato nelle versioni supportate di Windows.

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

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> </dl>

 


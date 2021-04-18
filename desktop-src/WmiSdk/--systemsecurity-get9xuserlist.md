---
description: Ottiene i diritti di accesso remoto per un elenco di singoli utenti in computer in cui sono in esecuzione versioni obsolete di Windows, in cui il controllo degli accessi tramite descrittori di sicurezza di Windows non è disponibile.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: 'Metodo __SystemSecurity:: Get9XUserList'
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
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315998"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_Metodo SystemSecurity:: Get9XUserList

Il metodo [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) ottiene i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo dell'accesso tramite i descrittori di sicurezza di Windows non è disponibile.

Questa funzione è simile a quella del descrittore di sicurezza, ma è più limitata. I gruppi non sono supportati e non è possibile controllare l'accesso locale perché l'utente locale ha sempre accesso completo. Sono consentite sia le voci di controllo di accesso sia Deny che Allow (ACE). per questo motivo, l'ordine ACE è importante nell'elenco di controllo di accesso discrezionale (DACL). Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ul* \[ out\]
</dt> <dd>

Matrice di utenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **HRESULT** che indica lo stato della chiamata al metodo. Nell'elenco seguente sono elencati i valori restituiti significativi per **Get9XUserList**. Per gli script e le applicazioni Visual Basic, il risultato può essere [OutParameters. returnValue](parsing-outparameters-objects.md). Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**WBEM \_ E \_ metodo \_ disabilitato**
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

[**\_\_SystemSecurity:: GetSd**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity:: SetD**](--systemsecurity-setsd.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> </dl>

 


---
description: Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza è rappresentato da un'istanza di \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Metodo SetSecurityDescriptor della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d44322820514fc676c1b3ad304375f5f3ce8966a73217c6505f24659914f7853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315628"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Metodo SetSecurityDescriptor della \_ \_ classe SystemSecurity

Il [**metodo SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza è rappresentato da un'istanza di [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Per altre informazioni, vedere [Modifica della sicurezza degli accessi in oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ Pollici\]
</dt> <dd>

Descrittore di sicurezza associato allo spazio dei nomi WMI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per altre informazioni, vedere [Codici restituiti WMI](wmi-return-codes.md) o [**WbemErrorEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)

<dl> <dt>

**0**
</dt> <dd>

Completamento.

</dd> <dt>

**2**
</dt> <dd>

L'utente non ha accesso alle informazioni richieste.

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto.

</dd> <dt>

**9**
</dt> <dd>

L'utente non dispone di privilegi adeguati per eseguire il metodo .

</dd> <dt>

**21**
</dt> <dd>

Un parametro specificato nella chiamata al metodo non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/a-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly) Per altre informazioni, vedere [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**Costanti dei privilegi**](privilege-constants.md) ed Esecuzione di operazioni con [privilegi](executing-privileged-operations.md).

È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**\_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo l'elenco SACL.

I valori seguenti in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL o il SACL o entrambi vengono aggiornati.

-   **\_edizione Standard DACL \_ PRESENTE**

    Indica che l'elenco DACL deve essere aggiornato. Se non è impostato, WMI mantiene il valore originale dell'elenco DACL.

-   **\_edizione Standard SACL \_ PRESENT**

    Indica che l'elenco di controllo di accesso condiviso deve essere aggiornato. Se non è impostato, WMI mantiene il valore originale dell'elenco di controllo di accesso condiviso. Per aggiornare il SACL, l'account deve avere il **privilegio SeSecurityPrivilege** abilitato. Per gli script, il nome del privilegio è **SeSecurityPrivilege**. Per altre informazioni, vedere [**Costanti dei privilegi**](privilege-constants.md).

Se le proprietà Trustee e Owner trustee del gruppo non sono **NULL,** vengono aggiornate. In caso contrario, WMI mantiene i valori originali. Per altre informazioni, vedere [Oggetti descrittori di sicurezza WMI](wmi-security-descriptor-objects.md).

Quando un nuovo SACL è **NULL** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione rimane invariato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Impostazione dei descrittori di sicurezza di Namepace](setting-namespace-security-descriptors.md)
</dt> </dl>

 


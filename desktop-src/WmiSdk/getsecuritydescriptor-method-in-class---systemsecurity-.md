---
description: Ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza viene restituito come istanza di \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Metodo GetSecurityDescriptor della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 77053174878db77409c525510acb54740ac8ad5c5c0505af5bf6ff8421cdf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050859"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Metodo GetSecurityDescriptor della \_ \_ classe SystemSecurity

Il **metodo GetSecurityDescriptor** ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza viene restituito come istanza di [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Per altre informazioni, vedere [Modifica della sicurezza degli accessi in oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ Cambio\]
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

[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly) Per altre informazioni, vedere [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**Costanti dei privilegi**](privilege-constants.md) ed Esecuzione di operazioni con [privilegi](executing-privileged-operations.md).

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

 


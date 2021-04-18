---
description: Ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza viene restituito come un'istanza di \_ \_ securityDescriptor.
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
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315224"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Metodo GetSecurityDescriptor della \_ \_ classe SystemSecurity

Il metodo **GetSecurityDescriptor** ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza viene restituito come un'istanza di [**\_ \_ securityDescriptor**](--securitydescriptor.md). Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore* \[ out\]
</dt> <dd>

Descrittore di sicurezza associato allo spazio dei nomi WMI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore. Per ulteriori informazioni, vedere [codici restituiti WMI](wmi-return-codes.md) o [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**0**
</dt> <dd>

Operazione completata.

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

L'utente non dispone di privilegi sufficienti per eseguire il metodo.

</dd> <dt>

**21**
</dt> <dd>

Un parametro specificato nella chiamata al metodo non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL. Per altre informazioni, vedere [**costanti Privilege**](privilege-constants.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).

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

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> </dl>

 


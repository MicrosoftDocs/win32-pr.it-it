---
description: Elenca i tipi ACE attualmente definiti.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de555170bc8b7c1594b38adaa95d19b7e9ace54c8241fc971ea9f5383cf3e115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785220"
---
# <a name="ace"></a>asso

Una **voce ACE** è una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) in un elenco di [*controllo*](/windows/desktop/SecGloss/a-gly) di accesso (ACL).

Nella tabella seguente sono elencati i tipi **ACE** attualmente definiti.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo ACE</th>
<th>Struttura</th>
<th>Tipo ACL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Accesso consentito</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="even">
<td><ul>
<li>Accesso consentito</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="odd">
<td><ul>
<li>Accesso consentito</li>
<li>Specifico dell'oggetto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="even">
<td><ul>
<li>Accesso consentito</li>
<li>Specifico dell'oggetto</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="odd">
<td><ul>
<li>Accesso negato</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="even">
<td><ul>
<li>Accesso negato</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="odd">
<td><ul>
<li>Accesso negato</li>
<li>Specifico dell'oggetto</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="even">
<td><ul>
<li>Accesso negato</li>
<li>Specifico dell'oggetto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></td>
<td>Discrezionale</td>
</tr>
<tr class="odd">
<td><ul>
<li>Allarme di sistema</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Allarme di sistema</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="odd">
<td><ul>
<li>Allarme di sistema</li>
<li>Specifico dell'oggetto</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Allarme di sistema</li>
<li>Specifico dell'oggetto</li>
</ul></td>
<td><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="odd">
<td><ul>
<li>Controllo del sistema</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Controllo del sistema</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="odd">
<td><ul>
<li>Controllo del sistema</li>
<li>Specifico dell'oggetto</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Controllo del sistema</li>
<li>Specifico dell'oggetto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
</tbody>
</table>



 

Le voci ACE di allarme di sistema e specifiche dell'oggetto non sono attualmente supportate.

> [!Note]  
> Ogni ACE inizia con una [**struttura ACE \_ HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Il formato dei dati che segue l'intestazione varia in base al tipo ACE specificato nell'intestazione.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**ACCESS \_ ALLOWED ACE (ACCESSO \_ CONSENTITO ACE)**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACE \_ ACCESSO \_ NEGATO**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**CONTROLLO DI \_ \_ ACE DI ALLARME DI SISTEMA**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**ACE \_ DI CONTROLLO \_ DEL SISTEMA**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>


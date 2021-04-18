---
description: Elenca i tipi ACE attualmente definiti.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310952"
---
# <a name="ace"></a>ACE

Una voce **ACE** è una [*voce di controllo*](/windows/desktop/SecGloss/a-gly) di accesso in un elenco di controllo di [*accesso*](/windows/desktop/SecGloss/a-gly) (ACL).

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
<li>Controllo di sistema</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Controllo di sistema</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="odd">
<td><ul>
<li>Controllo di sistema</li>
<li>Specifico dell'oggetto</li>
<li>Consente il callback durante il controllo di accesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Controllo di sistema</li>
<li>Specifico dell'oggetto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
</tbody>
</table>



 

Gli assi di allarme di sistema e di sistema specifici dell'oggetto non sono attualmente supportati.

> [!Note]  
> Ogni voce ACE inizia con una struttura di [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . Il formato dei dati che seguono l'intestazione varia a seconda del tipo di voce ACE specificato nell'intestazione.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**\_ACE consentito per l'accesso \_**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACE di accesso \_ negato \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**\_ACE allarme \_ sistema**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**\_ACE di controllo del sistema \_**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>


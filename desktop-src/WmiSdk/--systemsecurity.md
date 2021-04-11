---
description: Contiene metodi che consentono di accedere e modificare le impostazioni di sicurezza per uno spazio dei nomi.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: Classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132083"
---
# <a name="__systemsecurity-class"></a>\_\_Classe SystemSecurity

La classe di sistema **\_ \_ SystemSecurity** contiene metodi che consentono di accedere e modificare le impostazioni di sicurezza per uno spazio dei nomi. La classe **\_ \_ SystemSecurity** è una classe singleton in ogni spazio dei nomi.

> [!Note]  
> Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a>Members

La classe **\_ \_ SystemSecurity** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **\_ \_ SystemSecurity** dispone di questi metodi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></td>
<td style="text-align: left;">Ottiene un elenco di utenti a cui è consentito l'accesso remoto.<br/>
<blockquote>
[!Note]<br />
Questo metodo non funziona sulle versioni supportate di Windows. <a href="--systemsecurity-getsd.md"><strong>Viene</strong></a> invece utilizzato.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></td>
<td style="text-align: left;">Restituisce una maschera con ogni bit corrispondente a un diritto di accesso.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-getsd.md"><strong>Getsd ha</strong></a></td>
<td style="text-align: left;">Ottiene l' <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> per lo spazio dei nomi a cui è connesso l'utente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">Ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI associato all'istanza di <strong>__SystemSecurity</strong>. Il descrittore di sicurezza viene restituito come un'istanza di<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></td>
<td style="text-align: left;">Imposta un elenco di utenti a cui è consentito l'accesso remoto.<br/>
<blockquote>
[!Note]<br />
Questo metodo non funziona sulle versioni supportate di Windows. Utilizzare invece <a href="--systemsecurity-setsd.md"><strong>set</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-setsd.md"><strong>Setsd ha</strong></a></td>
<td style="text-align: left;">Imposta il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante. Il descrittore di sicurezza è rappresentato da un'istanza di <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

È possibile richiedere che le applicazioni e gli script client usino una connessione crittografata per l'autenticazione aggiungendo il qualificatore **RequiresEncryption** al file MOF che crea lo spazio dei nomi. È anche possibile modificare uno spazio dei nomi esistente aggiungendo questo attributo e compilare di nuovo il file con estensione MOF. Per ulteriori informazioni sull'utilizzo di **RequiresEncryption**, vedere la pagina relativa alla [richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Definizione dell'ereditarietà della sicurezza dello spazio dei nomi](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[Elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[**Descrittore di sicurezza \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>


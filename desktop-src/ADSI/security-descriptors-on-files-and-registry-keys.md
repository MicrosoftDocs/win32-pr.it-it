---
title: Descrittori di sicurezza per file e chiavi del Registro di sistema
description: Active Directory Service Interfaces (ADSI) può essere usato per gestire e proteggere i file system all'interno di un'organizzazione, inclusa la possibilità di impostare o modificare gli ACL su file o condivisioni file creati dagli utenti.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Descrittori di sicurezza su file e chiavi del Registro di sistema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae567e9550989153f0b85207be49a729bc0499c320f410c92fc993269d997da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333221"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a>Descrittori di sicurezza per file e chiavi del Registro di sistema

Active Directory Service Interfaces (ADSI) può essere usato per gestire e proteggere i file system all'interno di un'organizzazione, inclusa la possibilità di impostare o modificare gli ACL su file o condivisioni file creati dagli utenti. Le interfacce di sicurezza, ad esempio [**IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry,**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) impostano gli ACL in Active Directory, Exchange, file, condivisione file o oggetti chiave del Registro di sistema. Prima di usare queste interfacce, potrebbe essere necessario modificare il descrittore di sicurezza se usa un formato diverso dall'interfaccia o se non si dispone dei diritti di accesso al SACL del descrittore di sicurezza perché non si è membri del gruppo di amministratori della sicurezza.

Per ottenere, impostare o modificare il descrittore di sicurezza, usare [**l'interfaccia IADsSecurityUtility.**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) Questa interfaccia consente di recuperare un descrittore di sicurezza da varie risorse nel formato originale, ad esempio il formato ADSI [**IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)un descrittore di sicurezza non elaborato o come stringa esadecimale usata in Exchange 5.5. Una volta recuperato, è possibile convertirlo in un altro formato, ad esempio da un descrittore di sicurezza non elaborato a **IADsSecurityDescriptor**. È quindi possibile scrivere di nuovo il nuovo formato nella risorsa.

Alcuni dei valori [**della proprietà IADsAccessControlEntry,**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) ad esempio [**AccessMask**](iadsaccesscontrolentry-property-methods.md) e **AceFlags,** saranno diversi per tipi di oggetto diversi. Ad esempio, un oggetto Active Directory userà il membro **ADS \_ RIGHT GENERIC \_ \_ READ** dell'enumerazione [**ADS RIGHTS \_ \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) per la proprietà **IADsAccessControlEntry.AccessMask,** ma il diritto di accesso equivalente per un oggetto file è **FILE GENERIC \_ \_ READ**. Non è sicuro presupporre che tutti i valori delle proprietà siano gli stessi per gli oggetti di Active Directory e gli oggetti non Active Directory. L'elenco seguente mostra **le proprietà IADsAccessControlEntry** che differiscono per gli oggetti non Active Directory e in cui è possibile ottenere i valori appropriati.

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**Accessmask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Per altre informazioni e un elenco dei valori possibili per gli oggetti di condivisione file o file, vedere Sicurezza dei [file e diritti di accesso](/windows/desktop/FileIO/file-security-and-access-rights).

Per altre informazioni e un elenco dei valori possibili per gli oggetti del Registro di sistema, vedere Sicurezza e diritti di accesso delle chiavi [del Registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Per altre informazioni, vedere il **membro AceType** della [**struttura ACE \_ HEADER.**](/windows/desktop/api/winnt/ns-winnt-ace_header)

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Per altre informazioni, vedere il **membro AceFlags** della [**struttura ACE \_ HEADER.**](/windows/desktop/api/winnt/ns-winnt-ace_header)

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Bandiere**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Contiene zero o una combinazione di uno o più dei valori seguenti di WinNT.h.

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ TIPO \_ DI \_ OGGETTO PRESENT** (1)
</dt> <dd>

[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contiene un valore valido.

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ TIPO DI \_ OGGETTO \_ \_ EREDITATO PRESENTE** (2)
</dt> <dd>

[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contiene un valore valido.

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**Objecttype**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Per altre informazioni, vedere il membro **ObjectType** delle [**\_ \_ \_ ACE ACCESS DENIED OBJECT,**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace) [**ACCESS ALLOWED OBJECT \_ \_ \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)e strutture simili. Questa proprietà non deve essere impostata o modificata per gli oggetti non Active Directory.

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Per altre informazioni, vedere il membro **InheritedObjectType** di [**ACCESS \_ DENIED \_ OBJECT \_ ACE,**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace) [**ACCESS ALLOWED OBJECT \_ \_ \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)e strutture simili. Questa proprietà non deve essere impostata o modificata per gli oggetti non Active Directory.

</dd> </dl>

In [**genere, IADsSecurityUtility.GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) recupererà tutte le parti del descrittore di sicurezza, ad esempio proprietario, gruppo, SACL o DACL. Analogamente, [**IADsSecurityUtility.SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) sovrascriverà tutte le parti del descrittore di sicurezza per impostazione predefinita. È possibile usare la [**proprietà IADsSecurityUtility.SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) per specificare singole parti del descrittore di sicurezza da recuperare o impostare. Ad esempio, è possibile impostare **SecurityMask** su [**ADS \_ SECURITY INFO \_ \_ DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) prima di chiamare **GetSecurityDescriptor** per recuperare solo l'elenco DACL senza recuperare le altre parti del descrittore di sicurezza.

Per altre informazioni e un esempio di codice che usa [**l'interfaccia IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) per aggiungere una ACE a un file, vedere Codice di esempio per l'aggiunta di una [ACE a un file](example-code-for-adding-an-ace-to-a-file.md).

Il codice di esempio seguente fornisce gli identificatori costanti per gli oggetti file, condivisione file e Registro di sistema per le proprietà [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** e **Flags** da usare con Visual Basic e Microsoft Visual Basic Scripting Edition.


```VB
' Identifiers for the IADsAccessControlEntry.AccessMask property for file,
' file share, and registry objects.
Const DELETE = &H10000
Const READ_CONTROL = &H20000
Const WRITE_DAC = &H40000
Const WRITE_OWNER = &H80000
Const SYNCHRONIZE = &H100000

Const STANDARD_RIGHTS_REQUIRED = &HF0000

Const STANDARD_RIGHTS_READ = &H20000
Const STANDARD_RIGHTS_WRITE = &H20000
Const STANDARD_RIGHTS_EXECUTE = &H20000

Const STANDARD_RIGHTS_ALL = &H1F0000

Const SPECIFIC_RIGHTS_ALL = &HFFFF

' Identifiers for the IADsAccessControlEntry.AccessMask property for file and
' file share objects.
Const FILE_READ_DATA = &H1                  '  file & pipe
Const FILE_LIST_DIRECTORY = &H1             '  directory

Const FILE_WRITE_DATA = &H2                 '  file & pipe
Const FILE_ADD_FILE = &H2                   '  directory

Const FILE_APPEND_DATA = &H4                '  file
Const FILE_ADD_SUBDIRECTORY = &H4           '  directory
Const FILE_CREATE_PIPE_INSTANCE = &H4       '  named pipe

Const FILE_READ_EA = &H8                    '  file & directory

Const FILE_WRITE_EA = &H10                  '  file & directory

Const FILE_EXECUTE = &H20                   '  file
Const FILE_TRAVERSE = &H20                  '  directory

Const FILE_DELETE_CHILD = &H40              '  directory

Const FILE_READ_ATTRIBUTES = &H80           '  all

Const FILE_WRITE_ATTRIBUTES = &H100         '  all

Const FILE_ALL_ACCESS = STANDARD_RIGHTS_REQUIRED Or SYNCHRONIZE Or &H1FF

Const FILE_GENERIC_READ = STANDARD_RIGHTS_READ Or FILE_READ_DATA Or FILE_READ_ATTRIBUTES Or _
                          FILE_READ_EA Or SYNCHRONIZE

Const FILE_GENERIC_WRITE = STANDARD_RIGHTS_WRITE Or FILE_WRITE_DATA Or FILE_WRITE_ATTRIBUTES Or _
                           FILE_WRITE_EA Or FILE_APPEND_DATA Or SYNCHRONIZE

Const FILE_GENERIC_EXECUTE = STANDARD_RIGHTS_EXECUTE Or FILE_READ_ATTRIBUTES Or FILE_EXECUTE Or SYNCHRONIZE


' Identifiers for the IADsAccessControlEntry.AccessMask property for registry
' objects.
Const KEY_QUERY_VALUE = &H1
Const KEY_SET_VALUE = &H2
Const KEY_CREATE_SUB_KEY = &H4
Const KEY_ENUMERATE_SUB_KEYS = &H8
Const KEY_NOTIFY = &H10
Const KEY_CREATE_LINK = &H20
Const KEY_WOW64_32KEY = &H200
Const KEY_WOW64_64KEY = &H100
Const KEY_WOW64_RES = &H300

Const KEY_READ = ((STANDARD_RIGHTS_READ Or KEY_QUERY_VALUE Or KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY) And _
                  (Not SYNCHRONIZE))

Const KEY_WRITE = ((STANDARD_RIGHTS_WRITE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY) And (Not SYNCHRONIZE))

Const KEY_EXECUTE = ((KEY_READ) And (Not SYNCHRONIZE))

Const KEY_ALL_ACCESS = ((STANDARD_RIGHTS_ALL Or KEY_QUERY_VALUE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY Or _
                         KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY Or KEY_CREATE_LINK) And (Not SYNCHRONIZE))
    

' Identifiers for the IADsAccessControlEntry.AceFlags property for file and
' file share objects.
Const OBJECT_INHERIT_ACE = &H1
Const CONTAINER_INHERIT_ACE = &H2
Const NO_PROPAGATE_INHERIT_ACE = &H4
Const INHERIT_ONLY_ACE = &H8
Const INHERITED_ACE = &H10
    

' Identifiers for the IADsAccessControlEntry.Flags property.
Const ACE_OBJECT_TYPE_PRESENT = 1
Const ACE_INHERITED_OBJECT_TYPE_PRESENT = 2
```



 

 
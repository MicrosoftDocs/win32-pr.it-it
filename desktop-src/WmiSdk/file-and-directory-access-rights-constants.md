---
description: Le classi WMI che rappresentano file o directory, ad esempio Win32 \_ codecfile o CIM \_ DataFile, contengono una proprietà AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Costanti dei diritti di accesso a file e directory (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324876"
---
# <a name="file-and-directory-access-rights-constants"></a>Costanti dei diritti di accesso a file e directory

Le classi WMI che rappresentano file o directory, ad esempio [**Win32 \_ codecfile**](/windows/desktop/CIMWin32Prov/win32-codecfile) o [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contengono una proprietà **accessMask** . Questa proprietà contiene le impostazioni di bit che specificano i diritti di accesso che un utente o un gruppo deve avere per un accesso o operazioni specifiche sul file. Per ulteriori informazioni, vedere [diritti di accesso e sicurezza dei file](/windows/desktop/FileIO/file-security-and-access-rights) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

Le classi di file o directory contenenti una proprietà **accessMask** includono:

-   [**File di \_ DataFile CIM**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**\_Directory CIM**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**\_LOGICALFILE CIM**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**Codecfile Win32 \_**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**\_Directory Win32**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**\_NTEventLogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**\_Condivisione Win32**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**\_ShortcutFile Win32**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

Nell'elenco seguente sono elencati i valori dei diritti di accesso a file e directory nella proprietà **accessMask** . Questa proprietà è una bitmap.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE \_ letti \_ dati**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede il diritto di leggere i dati dal file.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_Directory elenco \_ file**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede il diritto di leggere i dati dal file. Per una directory, questo valore concede il diritto di elencare il contenuto della directory.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_dati di scrittura file \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede il diritto di scrivere i dati nel file.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**file \_ Aggiungi \_ file**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede il diritto di scrivere i dati nel file. Per una directory, questo valore concede il diritto di creare un file nella directory.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**\_dati Accodamento file \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede il diritto di accodare i dati al file. Per una directory, questo valore concede il diritto di creare una sottodirectory.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE \_ Aggiungi \_ sottodirectory**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede il diritto di accodare i dati al file. Per una directory, questo valore concede il diritto di creare una sottodirectory.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**\_lettura file \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Concede il diritto di leggere gli attributi estesi.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**\_scrittura file \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Concede il diritto di scrivere attributi estesi.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_esecuzione file**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede il diritto di eseguire un file.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**\_attraversamento file**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede il diritto di eseguire un file. Per una directory, la directory può essere attraversata.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_Elimina file \_ figlio**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Concede il diritto di eliminare una directory e tutti i file in esso contenuti (elementi figlio), anche se i file sono di sola lettura.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_attributi di lettura file \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Concede il diritto di leggere gli attributi del file.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_attributi di scrittura file \_**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Concede il diritto di modificare gli attributi del file.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**ELIMINARE**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Concede il diritto di eliminare l'oggetto.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**controllo di lettura \_**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Concede il diritto di leggere le informazioni nel descrittore di sicurezza per l'oggetto, senza includere le informazioni nell'elenco SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Concede il diritto di modificare l'elenco DACL nel descrittore di sicurezza dell'oggetto per l'oggetto.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ proprietario**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Concede il diritto di modificare il proprietario nel descrittore di sicurezza per l'oggetto.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SINCRONIZZARE**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Concede il diritto di utilizzare l'oggetto per la sincronizzazione. Questo consente a un processo di attendere fino a quando l'oggetto non è in stato segnalato. Alcuni tipi di oggetto non supportano questo diritto di accesso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 


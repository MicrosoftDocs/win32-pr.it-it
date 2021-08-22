---
description: Le classi WMI che rappresentano file o directory, ad esempio CodecFile Win32 o \_ CIM \_ DataFile, contengono una proprietà AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Costanti per i diritti di accesso a file e directory (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8678627b0f7d9ce2ed7f9c8e7e39c49bdcd3b6c3a8313f7d7b3c517c379093d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131383"
---
# <a name="file-and-directory-access-rights-constants"></a>Costanti per i diritti di accesso a file e directory

Le classi WMI che rappresentano file o directory, ad esempio [**\_ CodecFile Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile) o [**CIM \_ DataFile,**](/windows/desktop/CIMWin32Prov/cim-datafile)contengono **una proprietà AccessMask.** Questa proprietà contiene impostazioni di bit che specificano i diritti di accesso che un utente o un gruppo deve avere per operazioni o accessi specifici sul file. Per altre informazioni, vedere [Sicurezza dei file e diritti di accesso e](/windows/desktop/FileIO/file-security-and-access-rights) Modifica della sicurezza [dell'accesso per gli oggetti a protezione diretta.](changing-access-security-on-securable-objects.md)

Le classi di file o directory che contengono una **proprietà AccessMask** includono:

-   [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**CIM \_ Directory**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**CIM \_ LogicalFile**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**Win32 \_ Directory**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**Condivisione \_ Win32**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Win32 \_ ShortcutFile**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

Nell'elenco seguente sono elencati i valori per i diritti di accesso a file e directory nella **proprietà AccessMask.** Questa proprietà è una bitmap.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE \_ READ \_ DATA**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede il diritto di leggere i dati dal file.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**DIRECTORY \_ ELENCO \_ FILE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede il diritto di leggere i dati dal file. Per una directory, questo valore concede il diritto di elencare il contenuto della directory.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**DATI \_ DI SCRITTURA \_ FILE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede il diritto di scrivere dati nel file.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE \_ ADD \_ FILE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede il diritto di scrivere dati nel file. Per una directory, questo valore concede il diritto di creare un file nella directory.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE \_ APPEND \_ DATA**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede il diritto di aggiungere dati al file. Per una directory, questo valore concede il diritto di creare una sottodirectory.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE \_ ADD \_ SUBDIRECTORY**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede il diritto di aggiungere dati al file. Per una directory, questo valore concede il diritto di creare una sottodirectory.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE \_ READ \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Concede il diritto di leggere gli attributi estesi.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE \_ WRITE \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Concede il diritto di scrivere attributi estesi.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE \_ EXECUTE**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede il diritto di eseguire un file.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**ATTRAVERSAMENTO \_ FILE**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede il diritto di eseguire un file. Per una directory, la directory può essere attraversata.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE \_ DELETE \_ CHILD**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Concede il diritto di eliminare una directory e tutti i file in essa contenuti (relativi elementi figlio), anche se i file sono di sola lettura.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**ATTRIBUTI \_ DI LETTURA \_ FILE**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Concede il diritto di leggere gli attributi del file.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**ATTRIBUTI \_ DI SCRITTURA \_ FILE**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Concede il diritto di modificare gli attributi del file.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**Elimina**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Concede il diritto di eliminare l'oggetto.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**CONTROLLO \_ DI LETTURA**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Concede il diritto di leggere le informazioni nel descrittore di sicurezza per l'oggetto, senza includere le informazioni nell'elenco SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Concede il diritto di modificare l'elenco DACL nel descrittore di sicurezza dell'oggetto per l'oggetto.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE \_ OWNER**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Concede il diritto di modificare il proprietario nel descrittore di sicurezza per l'oggetto .


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizzare**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Concede il diritto di utilizzare l'oggetto per la sincronizzazione. In questo modo un processo può attendere fino a quando l'oggetto non è in stato segnalato. Alcuni tipi di oggetto non supportano questo diritto di accesso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 


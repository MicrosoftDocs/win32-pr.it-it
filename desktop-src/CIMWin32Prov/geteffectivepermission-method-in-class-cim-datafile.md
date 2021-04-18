---
description: Determina se il chiamante dispone delle autorizzazioni aggregate per l' \_ oggetto DataFile del file CIM e della condivisione in cui risiede il file o la directory, come specificato dall'argomento di autorizzazione. Questo metodo viene ereditato da \_ LOGICALFILE CIM.
ms.assetid: 57eadc2e-36ef-4d3c-932f-6f7fafb2b9a4
ms.tgt_platform: multiple
title: Metodo GetEffectivePermission della classe CIM_DataFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 109e4953b310f9465c4523a9e80ca401c225f885
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304686"
---
# <a name="geteffectivepermission-method-of-the-cim_datafile-class"></a>Metodo GetEffectivePermission della classe del file di \_ DataFile CIM

Il metodo **GetEffectivePermission** determina se il chiamante dispone delle autorizzazioni aggregate per l' [**oggetto \_ DataFile**](cim-datafile.md) del file CIM e della condivisione in cui risiede il file o la directory, come specificato dall'argomento di **autorizzazione** . Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Autorizzazioni* \[ in\]
</dt> <dd>

Elenco delle autorizzazioni di cui il chiamante può richiedere informazioni.

<dt>

<span id="FILE_READ_DATA__file_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LEGGERE la \_ directory dell'elenco di file (file) di dati ( \_ \_ Directory)** (1 (0x1))


</dt> <dd>

Concede il diritto di leggere i dati dal file. Per una directory, questo valore concede il diritto di elencare il contenuto della directory.

</dd> <dt>

<span id="FILE_WRITE_DATA__file_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE_FILE_ADD_FILE__DIRECTORY_"></span>**File \_ Scrivi file di \_ dati (file) \_ Aggiungi \_ file (directory)** (2 (0x2))


</dt> <dd>

Concede il diritto di scrivere i dati nel file. Per una directory, questo valore concede il diritto di creare un file nella directory.

</dd> <dt>

<span id="FILE_APPEND_DATA__file_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**File \_ ACCODA \_ file di dati (file) \_ Aggiungi \_ sottodirectory (directory)** (4 (0x4))


</dt> <dd>

Concede il diritto di accodare i dati al file. Per una directory, questo valore concede il diritto di creare una sottodirectory.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8 (0x8))


</dt> <dd>

Concede il diritto di leggere gli attributi estesi.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16 (0x10))


</dt> <dd>

Concede il diritto di scrivere attributi estesi.

</dd> <dt>

<span id="FILE_EXECUTE__file_FILE_TRAVERSE__directory_"></span><span id="file_execute__file_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file_FILE_TRAVERSE__directory_"></span><span id="file_execute__file_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_FILE_TRAVERSE__DIRECTORY_"></span>**File \_ Attraversamento FILE di esecuzione (file) ( \_ Directory)** (32 (0x20))


</dt> <dd>

Concede il diritto di eseguire un file. Per una directory, la directory può essere attraversata.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64 (0x40))


</dt> <dd>

Concede il diritto di eliminare una directory e tutti i file in esso contenuti, anche se i file sono di sola lettura.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128 (0x80))


</dt> <dd>

Concede il diritto di leggere gli attributi del file.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256 (0x100))


</dt> <dd>

Concede il diritto di modificare gli attributi del file.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Elimina** (65536 (0x10000))


</dt> <dd>

Concede l'accesso DELETE.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072 (0x20000))


</dt> <dd>

Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC** (262144 (0x40000))


</dt> <dd>

Concede l'accesso in scrittura all'ACL discrezionale.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288 (0x80000))


</dt> <dd>

Assegna il proprietario della scrittura.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576 (0x100000))


</dt> <dd>

Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la chiamata dispone dell'autorizzazione necessaria. in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Il metodo **GetEffectivePermission** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>Aclui. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di \_ DataFile CIM](geteffectivepermission-method-in-class-cim-datafile.md)
</dt> <dt>

[**File di \_ DataFile CIM**](cim-datafile.md)
</dt> <dt>

[Attività WMI: file e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 


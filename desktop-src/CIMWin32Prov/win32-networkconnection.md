---
description: Rappresenta una connessione di rete attiva in un ambiente basato su Windows.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Classe Win32_NetworkConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748911"
---
# <a name="win32_networkconnection-class"></a><span data-ttu-id="6030d-103">Win32 \_ NetworkConnection (classe)</span><span class="sxs-lookup"><span data-stu-id="6030d-103">Win32\_NetworkConnection class</span></span>

<span data-ttu-id="6030d-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkConnection Win32** rappresenta una connessione di rete attiva in un ambiente basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="6030d-104">The **Win32\_NetworkConnection** [WMI class](../wmisdk/retrieving-a-class.md)represents an active network connection in a Windows-based environment.</span></span>

<span data-ttu-id="6030d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6030d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6030d-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6030d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6030d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6030d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="6030d-108">Members</span><span class="sxs-lookup"><span data-stu-id="6030d-108">Members</span></span>

<span data-ttu-id="6030d-109">La classe **Win32 \_ NetworkConnection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6030d-109">The **Win32\_NetworkConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="6030d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6030d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6030d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6030d-111">Properties</span></span>

<span data-ttu-id="6030d-112">La classe **Win32 \_ NetworkConnection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6030d-112">The **Win32\_NetworkConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6030d-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="6030d-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6030d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-116">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6030d-116">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-117">Elenco di diritti di accesso al file o alla directory specificata dall'utente o dal gruppo per conto del quale viene restituita l'istanza.</span><span class="sxs-lookup"><span data-stu-id="6030d-117">List of access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="6030d-118">Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6030d-118">On FAT volumes, the **FULL\_ACCESS** value is returned instead, indicating no security has been set on the object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6030d-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="6030d-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-120">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="6030d-120">Grants the right to read data from the file.</span></span> <span data-ttu-id="6030d-121">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="6030d-121">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="6030d-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="6030d-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-123">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="6030d-123">Grants the right to write data to the file.</span></span> <span data-ttu-id="6030d-124">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="6030d-124">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="6030d-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory** (4)</span><span class="sxs-lookup"><span data-stu-id="6030d-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-126">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="6030d-126">Grants the right to append data to the file.</span></span> <span data-ttu-id="6030d-127">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="6030d-127">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="6030d-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="6030d-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-129">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="6030d-129">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="6030d-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="6030d-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-131">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="6030d-131">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="6030d-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="6030d-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-133">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="6030d-133">Grants the right to execute a file.</span></span> <span data-ttu-id="6030d-134">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="6030d-134">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="6030d-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="6030d-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-136">Concede il diritto di eliminare una directory e tutti i file in esso contenuti (elementi figlio), anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6030d-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="6030d-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="6030d-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-138">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="6030d-138">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="6030d-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="6030d-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-140">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="6030d-140">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="6030d-141"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="6030d-141"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-142">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="6030d-142">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="6030d-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="6030d-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-144">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="6030d-144">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="6030d-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="6030d-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-146">Concede l'accesso in scrittura all'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="6030d-146">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="6030d-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="6030d-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-148">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="6030d-148">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="6030d-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="6030d-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="6030d-150">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="6030d-150">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6030d-151">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6030d-151">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-154">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6030d-154">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-155">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6030d-155">A short textual description of the object.</span></span>

<span data-ttu-id="6030d-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6030d-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6030d-157">**Commento**</span><span class="sxs-lookup"><span data-stu-id="6030d-157">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-160">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*")</span><span class="sxs-lookup"><span data-stu-id="6030d-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|*lpComment*")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-161">Commento fornito dal provider di rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-161">Comment supplied by the network provider.</span></span>

</dd> <dt>

<span data-ttu-id="6030d-162">**ConnectionState**</span><span class="sxs-lookup"><span data-stu-id="6030d-162">**ConnectionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-165">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**use \_ info \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **Ui1 \_ status**")</span><span class="sxs-lookup"><span data-stu-id="6030d-165">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USE\_INFO\_1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1)\|**ui1\_status**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-166">Stato corrente della connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-166">Current state of the network connection.</span></span>

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="6030d-167">**Connesso** ("connesso")</span><span class="sxs-lookup"><span data-stu-id="6030d-167">**Connected** ("Connected")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6030d-168">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="6030d-168">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6030d-169">**Sospesa** ("sospesa")</span><span class="sxs-lookup"><span data-stu-id="6030d-169">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="6030d-170">**Disconnesso** ("disconnesso")</span><span class="sxs-lookup"><span data-stu-id="6030d-170">**Disconnected** ("Disconnected")</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="6030d-171">**Connessione** ("connessione")</span><span class="sxs-lookup"><span data-stu-id="6030d-171">**Connecting** ("Connecting")</span></span>


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

<span data-ttu-id="6030d-172">**Riconnessione** ("riconnessione")</span><span class="sxs-lookup"><span data-stu-id="6030d-172">**Reconnecting** ("Reconnecting")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6030d-173">**ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="6030d-173">**ConnectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-176">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**")</span><span class="sxs-lookup"><span data-stu-id="6030d-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwScope**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-177">Tipo di persistenza della connessione utilizzata per la connessione alla rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-177">Persistence type of the connection used for connecting to the network.</span></span>

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

<span data-ttu-id="6030d-178">**Connessione corrente** ("connessione corrente")</span><span class="sxs-lookup"><span data-stu-id="6030d-178">**Current Connection** ("Current Connection")</span></span>


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

<span data-ttu-id="6030d-179">**Connessione permanente** ("connessione permanente")</span><span class="sxs-lookup"><span data-stu-id="6030d-179">**Persistent Connection** ("Persistent Connection")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6030d-180">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6030d-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-183">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6030d-183">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-184">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6030d-184">A textual description of the object.</span></span>

<span data-ttu-id="6030d-185">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6030d-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6030d-186">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="6030d-186">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-189">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**")</span><span class="sxs-lookup"><span data-stu-id="6030d-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwDisplayType**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-190">L'oggetto di rete deve essere visualizzato in un'interfaccia utente di esplorazione della rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-190">Network object should be displayed in a network browsing user interface.</span></span>

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

<span data-ttu-id="6030d-191">**Dominio** ("dominio")</span><span class="sxs-lookup"><span data-stu-id="6030d-191">**Domain** ("Domain")</span></span>


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

<span data-ttu-id="6030d-192">**Generico** (generico)</span><span class="sxs-lookup"><span data-stu-id="6030d-192">**Generic** ("Generic")</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="6030d-193">**Server** ("Server")</span><span class="sxs-lookup"><span data-stu-id="6030d-193">**Server** ("Server")</span></span>


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

<span data-ttu-id="6030d-194">**Condividi** ("Condividi")</span><span class="sxs-lookup"><span data-stu-id="6030d-194">**Share** ("Share")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6030d-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6030d-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-196">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6030d-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-198">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="6030d-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-199">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="6030d-199">Indicates when the object was installed.</span></span> <span data-ttu-id="6030d-200">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="6030d-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6030d-201">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6030d-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6030d-202">**LocalName**</span><span class="sxs-lookup"><span data-stu-id="6030d-202">**LocalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-205">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**")</span><span class="sxs-lookup"><span data-stu-id="6030d-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpLocalName**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-206">Nome locale del dispositivo di rete connesso.</span><span class="sxs-lookup"><span data-stu-id="6030d-206">Local name of the connected network device.</span></span>

<span data-ttu-id="6030d-207">Esempio: "c: \\ public"</span><span class="sxs-lookup"><span data-stu-id="6030d-207">Example: "c:\\public"</span></span>

</dd> <dt>

<span data-ttu-id="6030d-208">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6030d-208">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-211">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span><span class="sxs-lookup"><span data-stu-id="6030d-211">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-212">Nome della connessione di rete corrente.</span><span class="sxs-lookup"><span data-stu-id="6030d-212">Name of the current network connection.</span></span> <span data-ttu-id="6030d-213">Si tratta della combinazione dei valori in **RemoteName** e **localName**.</span><span class="sxs-lookup"><span data-stu-id="6030d-213">It is the combination of the values in **RemoteName** and **LocalName**.</span></span>

<span data-ttu-id="6030d-214">Esempio: " \\ \\ NTRELEASE (c: \\ Public)"</span><span class="sxs-lookup"><span data-stu-id="6030d-214">Example: "\\\\NTRELEASE (c:\\public)"</span></span>

</dd> <dt>

<span data-ttu-id="6030d-215">**Persistente**</span><span class="sxs-lookup"><span data-stu-id="6030d-215">**Persistent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-216">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6030d-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-218">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Functions \| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span><span class="sxs-lookup"><span data-stu-id="6030d-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-219">La connessione verrà riconnessa automaticamente dal sistema operativo all'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="6030d-219">Connection will be reconnected automatically by the operating system on the next logon.</span></span>

</dd> <dt>

<span data-ttu-id="6030d-220">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="6030d-220">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-223">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**")</span><span class="sxs-lookup"><span data-stu-id="6030d-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpProvider**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-224">Nome del provider a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6030d-224">Name of the provider that owns the resource.</span></span> <span data-ttu-id="6030d-225">Questa proprietà può essere **null** se il nome del provider è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6030d-225">This property can be **NULL** if the provider name is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="6030d-226">**RemoteName**</span><span class="sxs-lookup"><span data-stu-id="6030d-226">**RemoteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-229">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="6030d-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-230">Nome della risorsa di rete remota per una risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-230">Remote network resource name for a network resource.</span></span> <span data-ttu-id="6030d-231">Per una connessione corrente o permanente, **RemoteName** contiene il nome di rete associato al nome del valore nella proprietà **localName** .</span><span class="sxs-lookup"><span data-stu-id="6030d-231">For a current or persistent connection, **RemoteName** contains the network name associated with the name of the value in the **LocalName** property.</span></span> <span data-ttu-id="6030d-232">Il nome in **RemoteName** deve rispettare le convenzioni di denominazione del provider di rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-232">The name in **RemoteName** must follow the network provider's naming conventions.</span></span>

<span data-ttu-id="6030d-233">Esempio: " \\ \\ NTRELEASE"</span><span class="sxs-lookup"><span data-stu-id="6030d-233">Example: "\\\\NTRELEASE"</span></span>

</dd> <dt>

<span data-ttu-id="6030d-234">**RemotePath**</span><span class="sxs-lookup"><span data-stu-id="6030d-234">**RemotePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-237">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="6030d-237">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-238">Percorso completo della risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-238">Full path to the network resource.</span></span>

<span data-ttu-id="6030d-239">Esempio: " \\ \\ infosrv1 \\ public"</span><span class="sxs-lookup"><span data-stu-id="6030d-239">Example: "\\\\infosrv1\\public"</span></span>

</dd> <dt>

<span data-ttu-id="6030d-240">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="6030d-240">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-243">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")</span><span class="sxs-lookup"><span data-stu-id="6030d-243">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwType**")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-244">Tipo di risorsa a cui eseguire l'enumerazione o la connessione.</span><span class="sxs-lookup"><span data-stu-id="6030d-244">Type of resource to enumerate or connect to.</span></span>

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

<span data-ttu-id="6030d-245">**Disco** ("disco")</span><span class="sxs-lookup"><span data-stu-id="6030d-245">**Disk** ("Disk")</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="6030d-246">**Stampa** ("stampa")</span><span class="sxs-lookup"><span data-stu-id="6030d-246">**Print** ("Print")</span></span>


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

<span data-ttu-id="6030d-247">**Any** ("any")</span><span class="sxs-lookup"><span data-stu-id="6030d-247">**Any** ("Any")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6030d-248">**Status**</span><span class="sxs-lookup"><span data-stu-id="6030d-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-251">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="6030d-251">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-252">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6030d-252">String that indicates the current status of the object.</span></span> <span data-ttu-id="6030d-253">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="6030d-253">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6030d-254">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="6030d-254">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6030d-255">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="6030d-255">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6030d-256">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="6030d-256">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6030d-257">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="6030d-257">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6030d-258">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="6030d-258">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6030d-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6030d-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6030d-260">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6030d-260">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6030d-261">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6030d-261">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6030d-262">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="6030d-262">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6030d-263">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="6030d-263">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6030d-264">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="6030d-264">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6030d-265">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="6030d-265">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6030d-266">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="6030d-266">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6030d-267">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="6030d-267">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6030d-268">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="6030d-268">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6030d-269">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="6030d-269">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6030d-270">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="6030d-270">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6030d-271">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="6030d-271">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6030d-272">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="6030d-272">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6030d-273">**UserName**</span><span class="sxs-lookup"><span data-stu-id="6030d-273">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6030d-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6030d-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6030d-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6030d-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6030d-276">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Functions \| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span><span class="sxs-lookup"><span data-stu-id="6030d-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span></span>
</dt> </dl>

<span data-ttu-id="6030d-277">Nome utente o nome utente predefinito utilizzato per stabilire una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="6030d-277">User name or the default user name used to establish a network connection.</span></span>

<span data-ttu-id="6030d-278">Esempio: "SYSTEM"</span><span class="sxs-lookup"><span data-stu-id="6030d-278">Example: "SYSTEM"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6030d-279">Commenti</span><span class="sxs-lookup"><span data-stu-id="6030d-279">Remarks</span></span>

<span data-ttu-id="6030d-280">La classe **Win32 \_ NetworkConnection** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6030d-280">The **Win32\_NetworkConnection** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6030d-281">Esempio</span><span class="sxs-lookup"><span data-stu-id="6030d-281">Examples</span></span>

<span data-ttu-id="6030d-282">Nell'esempio di codice VBScript seguente vengono recuperate le informazioni sulla connessione di rete locale.</span><span class="sxs-lookup"><span data-stu-id="6030d-282">The following VBScript code sample retrieves information on the local network connection.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
```



## <a name="requirements"></a><span data-ttu-id="6030d-283">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6030d-283">Requirements</span></span>



| <span data-ttu-id="6030d-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="6030d-284">Requirement</span></span> | <span data-ttu-id="6030d-285">Valore</span><span class="sxs-lookup"><span data-stu-id="6030d-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6030d-286">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6030d-286">Minimum supported client</span></span><br/> | <span data-ttu-id="6030d-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6030d-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6030d-288">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6030d-288">Minimum supported server</span></span><br/> | <span data-ttu-id="6030d-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6030d-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6030d-290">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6030d-290">Namespace</span></span><br/>                | <span data-ttu-id="6030d-291">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6030d-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6030d-292">MOF</span><span class="sxs-lookup"><span data-stu-id="6030d-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6030d-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6030d-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6030d-294">DLL</span><span class="sxs-lookup"><span data-stu-id="6030d-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6030d-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6030d-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6030d-296">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6030d-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6030d-297">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="6030d-297">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="6030d-298">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6030d-298">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

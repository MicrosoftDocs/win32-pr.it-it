---
description: La \_ classe della condivisione Win32 rappresenta una risorsa condivisa in un sistema di computer che esegue Windows. Potrebbe trattarsi di un'unità disco, di una stampante, di una comunicazione interprocesso o di un altro dispositivo condivisibile. Per ulteriori informazioni sul recupero delle classi WMI, vedere Recupero di una classe.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127319"
---
# <a name="win32_share-class"></a><span data-ttu-id="b8cef-105">\_Classe condivisione Win32</span><span class="sxs-lookup"><span data-stu-id="b8cef-105">Win32\_Share class</span></span>

<span data-ttu-id="b8cef-106">La classe della **\_ condivisione Win32** rappresenta una risorsa condivisa in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="b8cef-106">The **Win32\_Share** class represents a shared resource on a computer system running Windows.</span></span> <span data-ttu-id="b8cef-107">Potrebbe trattarsi di un'unità disco, di una stampante, di una comunicazione interprocesso o di un altro dispositivo condivisibile.</span><span class="sxs-lookup"><span data-stu-id="b8cef-107">This may be a disk drive, printer, interprocess communication, or other sharable device.</span></span> <span data-ttu-id="b8cef-108">Per ulteriori informazioni sul recupero delle classi WMI, vedere [recupero di una classe](../wmisdk/retrieving-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="b8cef-108">For more information about retrieving WMI classes, see [Retrieving a Class](../wmisdk/retrieving-a-class.md).</span></span>

<span data-ttu-id="b8cef-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b8cef-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b8cef-110">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b8cef-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cef-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8cef-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="b8cef-112">Members</span><span class="sxs-lookup"><span data-stu-id="b8cef-112">Members</span></span>

<span data-ttu-id="b8cef-113">La classe della **\_ condivisione Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b8cef-113">The **Win32\_Share** class has these types of members:</span></span>

-   [<span data-ttu-id="b8cef-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b8cef-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8cef-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b8cef-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8cef-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="b8cef-116">Methods</span></span>

<span data-ttu-id="b8cef-117">La classe della **\_ condivisione Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b8cef-117">The **Win32\_Share** class has these methods.</span></span>



| <span data-ttu-id="b8cef-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="b8cef-118">Method</span></span>                                                             | <span data-ttu-id="b8cef-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8cef-119">Description</span></span>                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8cef-120">**Creare**</span><span class="sxs-lookup"><span data-stu-id="b8cef-120">**Create**</span></span>](create-method-in-class-win32-share.md)               | <span data-ttu-id="b8cef-121">Metodo della classe che avvia la condivisione per una risorsa server.</span><span class="sxs-lookup"><span data-stu-id="b8cef-121">Class method that initiates sharing for a server resource.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="b8cef-122">**Delete**</span><span class="sxs-lookup"><span data-stu-id="b8cef-122">**Delete**</span></span>](delete-method-in-class-win32-share.md)               | <span data-ttu-id="b8cef-123">Metodo della classe che elimina un nome di condivisione dall'elenco di risorse condivise di un server, disconnettendo le connessioni alla risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="b8cef-123">Class method that deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span><br/>                                                                       |
| [<span data-ttu-id="b8cef-124">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="b8cef-124">**GetAccessMask**</span></span>](getaccessmask-method-in-class-win32-share.md) | <span data-ttu-id="b8cef-125">Restituisce i diritti di accesso alla condivisione utilizzata dall'utente o dal gruppo per conto del quale viene restituita l'istanza.</span><span class="sxs-lookup"><span data-stu-id="b8cef-125">Returns the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="b8cef-126">È consigliabile usare questo metodo al posto della proprietà **accessMask** , che è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="b8cef-126">You should use this method in place of the **AccessMask** property, which is always **NULL**.</span></span><br/> |
| [<span data-ttu-id="b8cef-127">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="b8cef-127">**SetShareInfo**</span></span>](setshareinfo-method-in-class-win32-share.md)   | <span data-ttu-id="b8cef-128">Metodo della classe che imposta i parametri di una risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="b8cef-128">Class method that sets the parameters of a shared resource.</span></span><br/>                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="b8cef-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b8cef-129">Properties</span></span>

<span data-ttu-id="b8cef-130">La classe della **\_ condivisione Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b8cef-130">The **Win32\_Share** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8cef-131">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="b8cef-131">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8cef-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-134">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b8cef-134">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-135">Questa proprietà è obsoleta e non viene più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b8cef-135">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="b8cef-136">Usare invece il metodo [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="b8cef-136">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="b8cef-137">Il valore della proprietà **accessMask** è impostato su **null** da WMI.</span><span class="sxs-lookup"><span data-stu-id="b8cef-137">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="b8cef-138">Per ulteriori informazioni sull'impostazione dell'accesso quando viene creata una condivisione, vedere il metodo [**create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="b8cef-138">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-139">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="b8cef-139">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b8cef-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-142">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ USA")</span><span class="sxs-lookup"><span data-stu-id="b8cef-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-143">Il numero di utenti simultanei per questa risorsa è stato limitato.</span><span class="sxs-lookup"><span data-stu-id="b8cef-143">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="b8cef-144">Se **true**, il valore nella proprietà **MaximumAllowed** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b8cef-144">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-145">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b8cef-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b8cef-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-148">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b8cef-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-149">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8cef-149">A short textual description of the object.</span></span>

<span data-ttu-id="b8cef-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8cef-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-151">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b8cef-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b8cef-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-154">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b8cef-154">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-155">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8cef-155">A textual description of the object.</span></span>

<span data-ttu-id="b8cef-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8cef-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8cef-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-158">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8cef-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-160">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b8cef-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-161">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="b8cef-161">Indicates when the object was installed.</span></span> <span data-ttu-id="b8cef-162">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="b8cef-162">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b8cef-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8cef-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-164">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="b8cef-164">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8cef-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-167">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ USA")</span><span class="sxs-lookup"><span data-stu-id="b8cef-167">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-168">Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="b8cef-168">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="b8cef-169">Il valore è valido solo se la proprietà **AllowMaximum** è impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="b8cef-169">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-170">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b8cef-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b8cef-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-173">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="b8cef-173">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-174">Alias assegnato a un percorso configurato come una condivisione in un computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="b8cef-174">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="b8cef-175">Esempio di Windows 2008: " \\ Server01 \\ public"-per windows Server 2008 è necessario inserire l'UNC nel nome.</span><span class="sxs-lookup"><span data-stu-id="b8cef-175">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-176">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="b8cef-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b8cef-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-179">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="b8cef-179">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-180">Percorso locale della condivisione di Windows.</span><span class="sxs-lookup"><span data-stu-id="b8cef-180">Local path of the Windows share.</span></span>

<span data-ttu-id="b8cef-181">Esempio: "C: \\ Program Files"</span><span class="sxs-lookup"><span data-stu-id="b8cef-181">Example: "C:\\Program Files"</span></span>

</dd> <dt>

<span data-ttu-id="b8cef-182">**Status**</span><span class="sxs-lookup"><span data-stu-id="b8cef-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b8cef-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-185">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b8cef-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-186">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8cef-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="b8cef-187">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="b8cef-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b8cef-188">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="b8cef-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b8cef-189">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="b8cef-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b8cef-190">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b8cef-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b8cef-191">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b8cef-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b8cef-192">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b8cef-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b8cef-193">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8cef-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8cef-194">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8cef-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b8cef-195">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b8cef-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b8cef-196">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b8cef-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8cef-197">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b8cef-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8cef-198">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b8cef-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b8cef-199">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b8cef-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b8cef-200">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b8cef-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b8cef-201">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b8cef-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b8cef-202">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b8cef-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b8cef-203">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b8cef-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b8cef-204">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b8cef-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b8cef-205">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b8cef-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b8cef-206">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b8cef-206">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8cef-207">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b8cef-207">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cef-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8cef-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8cef-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cef-210">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Condividi \_ informazioni \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| \_ tipo shi502")</span><span class="sxs-lookup"><span data-stu-id="b8cef-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="b8cef-211">Tipo di risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="b8cef-211">Type of resource being shared.</span></span> <span data-ttu-id="b8cef-212">I tipi includono le unità disco, le code di stampa, le comunicazioni interprocesso (IPC) e i dispositivi generali.</span><span class="sxs-lookup"><span data-stu-id="b8cef-212">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="b8cef-213">**Unità disco** (0)</span><span class="sxs-lookup"><span data-stu-id="b8cef-213">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="b8cef-214">**Coda di stampa** (1)</span><span class="sxs-lookup"><span data-stu-id="b8cef-214">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="b8cef-215">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="b8cef-215">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="b8cef-216">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="b8cef-216">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="b8cef-217">**Amministrazione unità disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="b8cef-217">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="b8cef-218">**Amministrazione coda di stampa** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="b8cef-218">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="b8cef-219">**Amministratore del dispositivo** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="b8cef-219">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="b8cef-220">**Amministratore IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="b8cef-220">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="b8cef-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b8cef-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b8cef-222">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8cef-222">Remarks</span></span>

<span data-ttu-id="b8cef-223">La classe della **\_ condivisione Win32** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8cef-223">The **Win32\_Share** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="b8cef-224">Il metodo create in questa classe è un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="b8cef-224">The Create method in this class is a static method.</span></span> <span data-ttu-id="b8cef-225">I metodi **Delete**, **GetAccessMask** e **SetShareInfo** sono tutti metodi di istanza.</span><span class="sxs-lookup"><span data-stu-id="b8cef-225">The **Delete**, **GetAccessMask** and **SetShareInfo** methods are all instance methods.</span></span>

<span data-ttu-id="b8cef-226">A seconda delle autorizzazioni di sicurezza, potrebbe non essere possibile recuperare tutte le proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b8cef-226">Depending on your security permissions, you may not be able to retrieve all of the properties of this class.</span></span> <span data-ttu-id="b8cef-227">Ad esempio, le proprietà **AllowMaximum**, **MaximumAllowed**, **path** e **Type** possono restituire null.</span><span class="sxs-lookup"><span data-stu-id="b8cef-227">For example, **AllowMaximum**, **MaximumAllowed**, **Path**, and **Type** properties may return null.</span></span> <span data-ttu-id="b8cef-228">In generale, gli utenti avanzati e gli amministratori potranno recuperare tutti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="b8cef-228">Generally speaking, Power Users and Administrators will be able to retrieve all property values.</span></span>

## <a name="examples"></a><span data-ttu-id="b8cef-229">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8cef-229">Examples</span></span>

<span data-ttu-id="b8cef-230">Il seguente esempio di[codice](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) di script Center elenca tutte le condivisioni in un computer ed elenca tutte le autorizzazioni di condivisione per ogni condivisione.</span><span class="sxs-lookup"><span data-stu-id="b8cef-230">The following Script Center[code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) lists all shares on a computer, and list all the share permissions for each share.</span></span>

<span data-ttu-id="b8cef-231">L'esempio [Get Share Information simile a Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell esegue una query su condivisione Win32 \_ e fornisce i risultati.</span><span class="sxs-lookup"><span data-stu-id="b8cef-231">The [Get Share Information similar to Win32\_Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell sample queries Win32\_Share and provides the results.</span></span>

<span data-ttu-id="b8cef-232">Nell'esempio di PowerShell seguente vengono visualizzate le condivisioni nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="b8cef-232">The following PowerShell sample displays the shares on the local system.</span></span>


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



<span data-ttu-id="b8cef-233">In alternativa, se si vuole filtrare più precisamente, è possibile usare il frammento di codice di PowerShell seguente:</span><span class="sxs-lookup"><span data-stu-id="b8cef-233">Alternately, if you wish to filter more precisely, you can use the following PowerShell snippet:</span></span>


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



<span data-ttu-id="b8cef-234">Nell'esempio VBScript seguente vengono visualizzate le condivisioni nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="b8cef-234">The Following VBScript sample displays the shares on the local system.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a><span data-ttu-id="b8cef-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8cef-235">Requirements</span></span>



| <span data-ttu-id="b8cef-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8cef-236">Requirement</span></span> | <span data-ttu-id="b8cef-237">Valore</span><span class="sxs-lookup"><span data-stu-id="b8cef-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cef-238">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8cef-238">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cef-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8cef-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8cef-240">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8cef-240">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cef-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8cef-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8cef-242">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8cef-242">Namespace</span></span><br/>                | <span data-ttu-id="b8cef-243">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b8cef-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8cef-244">MOF</span><span class="sxs-lookup"><span data-stu-id="b8cef-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8cef-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8cef-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8cef-246">DLL</span><span class="sxs-lookup"><span data-stu-id="b8cef-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8cef-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8cef-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8cef-248">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8cef-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cef-249">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="b8cef-249">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="b8cef-250">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b8cef-250">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b8cef-251">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="b8cef-251">WMI Tasks: Files and Folders</span></span>](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 

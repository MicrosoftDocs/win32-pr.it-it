---
description: La \_ classe Win32 ClusterShare rappresenta una risorsa condivisa in un cluster.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127354"
---
# <a name="win32_clustershare-class"></a><span data-ttu-id="e9395-103">Win32 \_ ClusterShare (classe)</span><span class="sxs-lookup"><span data-stu-id="e9395-103">Win32\_ClusterShare class</span></span>

<span data-ttu-id="e9395-104">\[La classe **Win32 \_ ClusterShare** è deprecata.</span><span class="sxs-lookup"><span data-stu-id="e9395-104">\[The **Win32\_ClusterShare** class is deprecated.</span></span> <span data-ttu-id="e9395-105">Usare invece le classi [**MSFT. \_ FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) e [**MSFT \_ SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) .\]</span><span class="sxs-lookup"><span data-stu-id="e9395-105">Please use the [**MSFT\_FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) and [**MSFT\_SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) classes instead.\]</span></span>

<span data-ttu-id="e9395-106">La \_ classe Win32 ClusterShare rappresenta una risorsa condivisa in un cluster.</span><span class="sxs-lookup"><span data-stu-id="e9395-106">The Win32\_ClusterShare class represents a shared resource on a cluster.</span></span>

<span data-ttu-id="e9395-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e9395-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9395-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9395-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
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
  string   ServerName;
};
```

## <a name="members"></a><span data-ttu-id="e9395-109">Members</span><span class="sxs-lookup"><span data-stu-id="e9395-109">Members</span></span>

<span data-ttu-id="e9395-110">La classe **Win32 \_ ClusterShare** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9395-110">The **Win32\_ClusterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="e9395-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9395-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e9395-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9395-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9395-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9395-113">Methods</span></span>

<span data-ttu-id="e9395-114">La classe **Win32 \_ ClusterShare** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e9395-114">The **Win32\_ClusterShare** class has these methods.</span></span>



| <span data-ttu-id="e9395-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="e9395-115">Method</span></span>                                                    | <span data-ttu-id="e9395-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9395-116">Description</span></span>                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="e9395-117">**Creare**</span><span class="sxs-lookup"><span data-stu-id="e9395-117">**Create**</span></span>](create-win32-clustershare.md)               | <span data-ttu-id="e9395-118">Crea una nuova istanza di **\_ ClusterShare Win32** .</span><span class="sxs-lookup"><span data-stu-id="e9395-118">Creates a new **Win32\_ClusterShare** instance.</span></span><br/>       |
| [<span data-ttu-id="e9395-119">**Delete**</span><span class="sxs-lookup"><span data-stu-id="e9395-119">**Delete**</span></span>](delete-win32-clustershare.md)               | <span data-ttu-id="e9395-120">Elimina un'istanza di **Win32 \_ ClusterShare** .</span><span class="sxs-lookup"><span data-stu-id="e9395-120">Deletes a **Win32\_ClusterShare** instance.</span></span><br/>           |
| [<span data-ttu-id="e9395-121">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="e9395-121">**GetAccessMask**</span></span>](getaccessmask-win32-clustershare.md) | <span data-ttu-id="e9395-122">Restituisce una bitmap con i diritti di accesso alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="e9395-122">Returns a bitmap with the access rights to the share.</span></span><br/> |
| [<span data-ttu-id="e9395-123">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="e9395-123">**SetShareInfo**</span></span>](setshareinfo-win32-clustershare.md)   | <span data-ttu-id="e9395-124">Imposta i parametri della risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="e9395-124">Sets the parameters of the shared resource.</span></span><br/>           |



 

### <a name="properties"></a><span data-ttu-id="e9395-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9395-125">Properties</span></span>

<span data-ttu-id="e9395-126">La classe **Win32 \_ ClusterShare** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9395-126">The **Win32\_ClusterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9395-127">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="e9395-127">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9395-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-130">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e9395-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e9395-131">Questa proprietà è obsoleta e non viene più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9395-131">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="e9395-132">Usare invece il metodo [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="e9395-132">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="e9395-133">Il valore della proprietà **accessMask** è impostato su **null** da WMI.</span><span class="sxs-lookup"><span data-stu-id="e9395-133">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="e9395-134">Per ulteriori informazioni sull'impostazione dell'accesso quando viene creata una condivisione, vedere il metodo [**create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="e9395-134">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

<span data-ttu-id="e9395-135">Questa proprietà viene ereditata [**dalla \_ condivisione Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-135">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-136">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="e9395-136">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9395-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ USA")</span><span class="sxs-lookup"><span data-stu-id="e9395-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-140">Il numero di utenti simultanei per questa risorsa è stato limitato.</span><span class="sxs-lookup"><span data-stu-id="e9395-140">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="e9395-141">Se **true**, il valore nella proprietà **MaximumAllowed** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e9395-141">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

<span data-ttu-id="e9395-142">Questa proprietà viene ereditata [**dalla \_ condivisione Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-142">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-143">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e9395-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9395-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-146">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e9395-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-147">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9395-147">A short textual description of the object.</span></span>

<span data-ttu-id="e9395-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-149">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e9395-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9395-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-152">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e9395-152">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-153">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9395-153">A textual description of the object.</span></span>

<span data-ttu-id="e9395-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-155">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e9395-155">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-156">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9395-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-158">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="e9395-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-159">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="e9395-159">Indicates when the object was installed.</span></span> <span data-ttu-id="e9395-160">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="e9395-160">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e9395-161">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-162">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="e9395-162">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9395-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-165">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ USA")</span><span class="sxs-lookup"><span data-stu-id="e9395-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-166">Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="e9395-166">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="e9395-167">Il valore è valido solo se la proprietà **AllowMaximum** è impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="e9395-167">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

<span data-ttu-id="e9395-168">Questa proprietà viene ereditata [**dalla \_ condivisione Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-168">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-169">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e9395-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9395-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-172">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ info \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="e9395-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-173">Alias assegnato a un percorso configurato come una condivisione in un computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="e9395-173">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="e9395-174">Esempio di Windows 2008: " \\ Server01 \\ public"-per windows Server 2008 è necessario inserire l'UNC nel nome.</span><span class="sxs-lookup"><span data-stu-id="e9395-174">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

<span data-ttu-id="e9395-175">Questa proprietà viene ereditata [**dalla \_ condivisione Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-175">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-176">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="e9395-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9395-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-179">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="e9395-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-180">Percorso locale della condivisione di Windows.</span><span class="sxs-lookup"><span data-stu-id="e9395-180">Local path of the Windows share.</span></span>

<span data-ttu-id="e9395-181">Esempio: "C: \\ Program Files"</span><span class="sxs-lookup"><span data-stu-id="e9395-181">Example: "C:\\Program Files"</span></span>

<span data-ttu-id="e9395-182">Questa proprietà viene ereditata [**dalla \_ condivisione Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-182">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9395-183">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="e9395-183">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9395-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-186">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ info \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName")</span><span class="sxs-lookup"><span data-stu-id="e9395-186">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)\|shi503\_servername")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-187">Server del cluster in cui è ospitata la condivisione.</span><span class="sxs-lookup"><span data-stu-id="e9395-187">The cluster server on which the share is hosted.</span></span>

</dd> <dt>

<span data-ttu-id="e9395-188">**Status**</span><span class="sxs-lookup"><span data-stu-id="e9395-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9395-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-191">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e9395-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-192">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9395-192">String that indicates the current status of the object.</span></span> <span data-ttu-id="e9395-193">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="e9395-193">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e9395-194">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="e9395-194">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e9395-195">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="e9395-195">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e9395-196">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="e9395-196">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e9395-197">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="e9395-197">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e9395-198">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="e9395-198">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e9395-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e9395-200">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9395-200">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e9395-201">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e9395-201">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e9395-202">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="e9395-202">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e9395-203">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="e9395-203">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9395-204">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e9395-204">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e9395-205">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="e9395-205">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e9395-206">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e9395-206">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e9395-207">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="e9395-207">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e9395-208">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="e9395-208">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e9395-209">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="e9395-209">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e9395-210">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="e9395-210">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e9395-211">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="e9395-211">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e9395-212">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="e9395-212">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9395-213">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e9395-213">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9395-214">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9395-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9395-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9395-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9395-216">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Condividi \_ informazioni \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| \_ tipo shi502")</span><span class="sxs-lookup"><span data-stu-id="e9395-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="e9395-217">Tipo di risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="e9395-217">Type of resource being shared.</span></span> <span data-ttu-id="e9395-218">I tipi includono le unità disco, le code di stampa, le comunicazioni interprocesso (IPC) e i dispositivi generali.</span><span class="sxs-lookup"><span data-stu-id="e9395-218">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<span data-ttu-id="e9395-219">Questa proprietà viene ereditata [**dalla \_ condivisione Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="e9395-219">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="e9395-220">**Unità disco** (0)</span><span class="sxs-lookup"><span data-stu-id="e9395-220">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="e9395-221">**Coda di stampa** (1)</span><span class="sxs-lookup"><span data-stu-id="e9395-221">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="e9395-222">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="e9395-222">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="e9395-223">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="e9395-223">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="e9395-224">**Amministrazione unità disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="e9395-224">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="e9395-225">**Amministrazione coda di stampa** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="e9395-225">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="e9395-226">**Amministratore del dispositivo** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="e9395-226">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="e9395-227">**Amministratore IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="e9395-227">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="e9395-228"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e9395-228"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e9395-229">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9395-229">Requirements</span></span>



| <span data-ttu-id="e9395-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9395-230">Requirement</span></span> | <span data-ttu-id="e9395-231">Valore</span><span class="sxs-lookup"><span data-stu-id="e9395-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9395-232">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9395-232">Minimum supported client</span></span><br/> | <span data-ttu-id="e9395-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9395-233">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e9395-234">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9395-234">Minimum supported server</span></span><br/> | <span data-ttu-id="e9395-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9395-235">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e9395-236">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9395-236">Namespace</span></span><br/>                | <span data-ttu-id="e9395-237">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e9395-237">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9395-238">MOF</span><span class="sxs-lookup"><span data-stu-id="e9395-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9395-239"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9395-239"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9395-240">DLL</span><span class="sxs-lookup"><span data-stu-id="e9395-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9395-241"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9395-241"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9395-242">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9395-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9395-243">**\_Condivisione Win32**</span><span class="sxs-lookup"><span data-stu-id="e9395-243">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 


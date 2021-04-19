---
description: Rappresenta i parametri per la copia di un file dall'host nel guest.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Classe Msvm_CopyFileToGuestSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317193"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a><span data-ttu-id="a9a21-103">\_Classe MSVM CopyFileToGuestSettingData</span><span class="sxs-lookup"><span data-stu-id="a9a21-103">Msvm\_CopyFileToGuestSettingData class</span></span>

<span data-ttu-id="a9a21-104">Rappresenta i parametri per la copia di un file dall'host nel guest.</span><span class="sxs-lookup"><span data-stu-id="a9a21-104">Represents the parameters for copying a file from the host into the guest.</span></span> <span data-ttu-id="a9a21-105">Questa classe deriva da [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9a21-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="a9a21-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a9a21-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a21-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9a21-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="a9a21-108">Members</span><span class="sxs-lookup"><span data-stu-id="a9a21-108">Members</span></span>

<span data-ttu-id="a9a21-109">La **classe \_ CopyFileToGuestSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a9a21-109">The **Msvm\_CopyFileToGuestSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a9a21-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a9a21-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9a21-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a9a21-111">Properties</span></span>

<span data-ttu-id="a9a21-112">La **classe \_ CopyFileToGuestSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9a21-112">The **Msvm\_CopyFileToGuestSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9a21-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a9a21-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9a21-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-116">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a9a21-116">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9a21-117">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a9a21-118">**CreateFullPath**</span><span class="sxs-lookup"><span data-stu-id="a9a21-118">**CreateFullPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-119">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a9a21-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-121">Indica se è necessario creare directory mancanti nel percorso del file di destinazione prima di copiare il file.</span><span class="sxs-lookup"><span data-stu-id="a9a21-121">Indicates whether missing directories in the destination file's path must be created before copying the file.</span></span>

</dd> <dt>

<span data-ttu-id="a9a21-122">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a9a21-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9a21-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-125">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9a21-125">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a9a21-126">**DestinationPath**</span><span class="sxs-lookup"><span data-stu-id="a9a21-126">**DestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9a21-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-129">Percorso completo del file di destinazione da copiare.</span><span class="sxs-lookup"><span data-stu-id="a9a21-129">The complete path of the destination file to be copied.</span></span> <span data-ttu-id="a9a21-130">Il file di destinazione deve essere accessibile al Guest e può contenere variabili di ambiente, che vengono espanse dal Guest.</span><span class="sxs-lookup"><span data-stu-id="a9a21-130">This destination file must be accessible to the guest and can contain environment variables, which are expanded by the guest.</span></span> <span data-ttu-id="a9a21-131">Se il percorso specificato è una directory esistente nel guest, il file di destinazione viene creato in questa directory.</span><span class="sxs-lookup"><span data-stu-id="a9a21-131">If the path specified is an existing directory in the guest, the destination file is created in this directory.</span></span> <span data-ttu-id="a9a21-132">In questo caso, il nome del file da **SourcePath** viene usato come nome del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a9a21-132">In this case, the file name from **SourcePath** is used as the destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="a9a21-133">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a9a21-133">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9a21-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-136">Nome visualizzato per questa istanza di SettingData.</span><span class="sxs-lookup"><span data-stu-id="a9a21-136">The display name for this instance of SettingData.</span></span> <span data-ttu-id="a9a21-137">Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="a9a21-137">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="a9a21-138">Nota: non è necessario che il nome sia univoco all'interno di uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a9a21-138">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="a9a21-139">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9a21-139">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9a21-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-142">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="a9a21-142">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-143">All'interno dell'ambito dello spazio dei nomi di creazione di istanze, InstanceID indica in modo opaco e univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a9a21-143">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a9a21-144">Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente: *OrgID*:*localizzato* in cui *OrgID* e *LocalId* sono separati da due punti (:) e dove *OrgID* deve includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità di business da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="a9a21-144">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="a9a21-145">(Questo requisito è simile a *SchemaName* \_ Struttura *ClassName* dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, *OrgID* non deve contenere i due punti (:).</span><span class="sxs-lookup"><span data-stu-id="a9a21-145">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="a9a21-146">Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono comparire tra *OrgID* e *localizzato*.</span><span class="sxs-lookup"><span data-stu-id="a9a21-146">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="a9a21-147">*Localizzato* viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti.</span><span class="sxs-lookup"><span data-stu-id="a9a21-147">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="a9a21-148">Se non viene utilizzato l'algoritmo preferenziale precedente, l'entità di definizione deve garantire che il InstanceID risultante non venga riutilizzato in alcun InstanceID prodotto da questo o da altri provider per lo spazio dei nomi di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="a9a21-148">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="a9a21-149">Per le istanze definite da DMTF, è necessario usare l'algoritmo "preferenziale" con *OrgID* impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="a9a21-149">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="a9a21-150">**OverwriteExisting**</span><span class="sxs-lookup"><span data-stu-id="a9a21-150">**OverwriteExisting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-151">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a9a21-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-153">Indica se è necessario sovrascrivere un file di destinazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a9a21-153">Indicates whether an existing destination file must be overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="a9a21-154">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="a9a21-154">**SourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a21-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9a21-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9a21-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9a21-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9a21-157">Percorso completo del file di origine da copiare.</span><span class="sxs-lookup"><span data-stu-id="a9a21-157">The complete path of the source file to be copied.</span></span> <span data-ttu-id="a9a21-158">Questo file di origine deve essere accessibile all'host Hyper-V e può contenere variabili di ambiente, che vengono espanse dall'host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a9a21-158">This source file must be accessible to the Hyper-V host and can contain environment variables, which are expanded by the Hyper-V host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9a21-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9a21-159">Requirements</span></span>



| <span data-ttu-id="a9a21-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a21-160">Requirement</span></span> | <span data-ttu-id="a9a21-161">Valore</span><span class="sxs-lookup"><span data-stu-id="a9a21-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a21-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9a21-162">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a21-163">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9a21-163">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a9a21-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9a21-164">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a21-165">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9a21-165">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a9a21-166">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a9a21-166">Namespace</span></span><br/>                | <span data-ttu-id="a9a21-167">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a9a21-167">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a9a21-168">MOF</span><span class="sxs-lookup"><span data-stu-id="a9a21-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9a21-169"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9a21-169"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9a21-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a9a21-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a21-171"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9a21-171"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9a21-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9a21-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a21-173">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="a9a21-173">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="a9a21-174">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9a21-174">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 


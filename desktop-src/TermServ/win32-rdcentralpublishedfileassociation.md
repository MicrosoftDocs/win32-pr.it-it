---
title: Classe Win32_RDCentralPublishedFileAssociation
description: Informazioni per un'estensione di file associata a un'applicazione.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDCentralPublishedFileAssociation Servizi Desktop remoto
- Classe Win32_RDCentralPublishedFileAssociation Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478850"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a><span data-ttu-id="f305f-105">Win32 \_ RDCentralPublishedFileAssociation (classe)</span><span class="sxs-lookup"><span data-stu-id="f305f-105">Win32\_RDCentralPublishedFileAssociation class</span></span>

<span data-ttu-id="f305f-106">Informazioni per un'estensione di file associata a un'applicazione</span><span class="sxs-lookup"><span data-stu-id="f305f-106">Info for a file extension associated with an application</span></span>

<span data-ttu-id="f305f-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f305f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f305f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f305f-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="f305f-109">Members</span><span class="sxs-lookup"><span data-stu-id="f305f-109">Members</span></span>

<span data-ttu-id="f305f-110">La classe **Win32 \_ RDCentralPublishedFileAssociation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f305f-110">The **Win32\_RDCentralPublishedFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="f305f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f305f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f305f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f305f-112">Properties</span></span>

<span data-ttu-id="f305f-113">La classe **Win32 \_ RDCentralPublishedFileAssociation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f305f-113">The **Win32\_RDCentralPublishedFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f305f-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="f305f-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f305f-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f305f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f305f-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f305f-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f305f-117">Alias dell'associazione di file RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f305f-117">Alias of the file association's RemoteApp.</span></span>

</dd> <dt>

<span data-ttu-id="f305f-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="f305f-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f305f-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f305f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f305f-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f305f-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f305f-121">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f305f-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f305f-122">Nome dell'estensione, ad esempio. txt.</span><span class="sxs-lookup"><span data-stu-id="f305f-122">Name of the extension (e.g. .txt).</span></span>

</dd> <dt>

<span data-ttu-id="f305f-123">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="f305f-123">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f305f-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f305f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f305f-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f305f-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f305f-126">Alias della farm RemoteApp's dell'associazione file</span><span class="sxs-lookup"><span data-stu-id="f305f-126">Alias of the file association's RemoteApp's Farm</span></span>

</dd> <dt>

<span data-ttu-id="f305f-127">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="f305f-127">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f305f-128">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f305f-128">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f305f-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f305f-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f305f-130">Contenuto dell'icona per questa associazione di file.</span><span class="sxs-lookup"><span data-stu-id="f305f-130">Contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="f305f-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="f305f-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f305f-132">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f305f-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f305f-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f305f-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f305f-134">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="f305f-134">Reserved for future use.</span></span> <span data-ttu-id="f305f-135">Sarà sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="f305f-135">Will always be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="f305f-136">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="f305f-136">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f305f-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f305f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f305f-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f305f-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f305f-139">Suggerimento per aprire i documenti con questa associazione di file.</span><span class="sxs-lookup"><span data-stu-id="f305f-139">Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f305f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f305f-140">Requirements</span></span>



| <span data-ttu-id="f305f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f305f-141">Requirement</span></span> | <span data-ttu-id="f305f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="f305f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f305f-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f305f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f305f-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f305f-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f305f-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f305f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f305f-146">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f305f-146">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="f305f-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f305f-147">Namespace</span></span><br/>                | <span data-ttu-id="f305f-148">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f305f-148">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f305f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f305f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f305f-150"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f305f-150"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f305f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f305f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f305f-152"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f305f-152"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 


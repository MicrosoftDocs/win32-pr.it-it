---
title: Classe Win32_RDFileAssociation
description: Rappresenta un'associazione del tipo di file per un RemoteApp.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDFileAssociation Servizi Desktop remoto
- Classe Win32_RDFileAssociation Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964083"
---
# <a name="win32_rdfileassociation-class"></a><span data-ttu-id="a19f0-105">Win32 \_ RDFileAssociation (classe)</span><span class="sxs-lookup"><span data-stu-id="a19f0-105">Win32\_RDFileAssociation class</span></span>

<span data-ttu-id="a19f0-106">Rappresenta un'associazione del tipo di file per un RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a19f0-106">Represents a file type association for a RemoteApp.</span></span>

<span data-ttu-id="a19f0-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a19f0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a19f0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a19f0-108">Syntax</span></span>

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="a19f0-109">Members</span><span class="sxs-lookup"><span data-stu-id="a19f0-109">Members</span></span>

<span data-ttu-id="a19f0-110">La classe **Win32 \_ RDFileAssociation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a19f0-110">The **Win32\_RDFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="a19f0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a19f0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a19f0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a19f0-112">Properties</span></span>

<span data-ttu-id="a19f0-113">La classe **Win32 \_ RDFileAssociation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a19f0-113">The **Win32\_RDFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a19f0-114">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="a19f0-114">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19f0-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a19f0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a19f0-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19f0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a19f0-117">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="a19f0-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a19f0-118">Nome dell'estensione del nome file, ad esempio. txt.</span><span class="sxs-lookup"><span data-stu-id="a19f0-118">The name of the file name extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="a19f0-119">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="a19f0-119">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19f0-120">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a19f0-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a19f0-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19f0-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19f0-122">Contenuto dell'icona per questa associazione di file.</span><span class="sxs-lookup"><span data-stu-id="a19f0-122">The contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="a19f0-123">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="a19f0-123">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19f0-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a19f0-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a19f0-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19f0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19f0-126">Indice dell'icona nel file.</span><span class="sxs-lookup"><span data-stu-id="a19f0-126">The index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="a19f0-127">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="a19f0-127">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19f0-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a19f0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a19f0-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19f0-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19f0-130">Percorso del file dell'icona per questa associazione di file.</span><span class="sxs-lookup"><span data-stu-id="a19f0-130">The file path to the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="a19f0-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="a19f0-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19f0-132">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a19f0-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a19f0-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19f0-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19f0-134">Indica se l'associazione è per un gestore primario.</span><span class="sxs-lookup"><span data-stu-id="a19f0-134">Indicates whether this association is for a primary handler.</span></span>

</dd> <dt>

<span data-ttu-id="a19f0-135">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="a19f0-135">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19f0-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a19f0-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a19f0-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19f0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19f0-138">Hint che consente di aprire i documenti con questa associazione di file.</span><span class="sxs-lookup"><span data-stu-id="a19f0-138">The Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a19f0-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a19f0-139">Requirements</span></span>



| <span data-ttu-id="a19f0-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a19f0-140">Requirement</span></span> | <span data-ttu-id="a19f0-141">Valore</span><span class="sxs-lookup"><span data-stu-id="a19f0-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a19f0-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a19f0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a19f0-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a19f0-143">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a19f0-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a19f0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a19f0-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a19f0-145">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="a19f0-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a19f0-146">Namespace</span></span><br/>                | <span data-ttu-id="a19f0-147">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a19f0-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a19f0-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a19f0-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a19f0-149"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a19f0-149"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="a19f0-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a19f0-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a19f0-151"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a19f0-151"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 






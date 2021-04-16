---
title: Classe Win32_RDAllowListFileAssociation
description: Descrive un'associazione del tipo di file pubblicato con un RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDAllowListFileAssociation Servizi Desktop remoto
- Classe Win32_RDAllowListFileAssociation Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476697"
---
# <a name="win32_rdallowlistfileassociation-class"></a><span data-ttu-id="fda06-105">Win32 \_ RDAllowListFileAssociation (classe)</span><span class="sxs-lookup"><span data-stu-id="fda06-105">Win32\_RDAllowListFileAssociation class</span></span>

<span data-ttu-id="fda06-106">Descrive un'associazione del tipo di file pubblicato con un RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fda06-106">Describes a published file type association with a RemoteApp.</span></span>

<span data-ttu-id="fda06-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fda06-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda06-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fda06-108">Syntax</span></span>

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a><span data-ttu-id="fda06-109">Members</span><span class="sxs-lookup"><span data-stu-id="fda06-109">Members</span></span>

<span data-ttu-id="fda06-110">La classe **Win32 \_ RDAllowListFileAssociation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fda06-110">The **Win32\_RDAllowListFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="fda06-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fda06-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fda06-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fda06-112">Properties</span></span>

<span data-ttu-id="fda06-113">La classe **Win32 \_ RDAllowListFileAssociation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fda06-113">The **Win32\_RDAllowListFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fda06-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="fda06-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda06-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fda06-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fda06-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fda06-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fda06-117">Alias del RemoteApp associato all'estensione.</span><span class="sxs-lookup"><span data-stu-id="fda06-117">Alias of the RemoteApp associated with the extension.</span></span>

</dd> <dt>

<span data-ttu-id="fda06-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="fda06-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda06-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fda06-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fda06-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fda06-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fda06-121">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="fda06-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fda06-122">Nome dell'estensione, ad esempio. txt.</span><span class="sxs-lookup"><span data-stu-id="fda06-122">Name of the extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="fda06-123">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="fda06-123">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda06-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fda06-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fda06-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fda06-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fda06-126">Suggerimento per aprire documenti con questa associazione di file</span><span class="sxs-lookup"><span data-stu-id="fda06-126">Hint to help open documents with this file association</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fda06-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fda06-127">Requirements</span></span>



| <span data-ttu-id="fda06-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fda06-128">Requirement</span></span> | <span data-ttu-id="fda06-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fda06-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fda06-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fda06-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fda06-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fda06-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fda06-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fda06-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fda06-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fda06-133">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="fda06-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fda06-134">Namespace</span></span><br/>                | <span data-ttu-id="fda06-135">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fda06-135">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fda06-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fda06-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fda06-137"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fda06-137"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="fda06-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fda06-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fda06-139"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fda06-139"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 






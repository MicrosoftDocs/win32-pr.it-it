---
title: Classe MDM_Personalization
description: La \_ classe di personalizzazione MDM viene utilizzata per impostare la schermata di blocco e le immagini di sfondo del desktop. L'impostazione di questi criteri impedisce inoltre all'utente di modificare l'immagine.
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- Classe MDM_Personalization
- Classe MDM_Personalization, descritta
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78986422cce15d750e1ae678aef352bbb369bfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964025"
---
# <a name="mdm_personalization-class"></a><span data-ttu-id="b22cf-106">\_Classe di personalizzazione MDM</span><span class="sxs-lookup"><span data-stu-id="b22cf-106">MDM\_Personalization class</span></span>

<span data-ttu-id="b22cf-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b22cf-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b22cf-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b22cf-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b22cf-109">La \_ classe di personalizzazione MDM viene utilizzata per impostare la schermata di blocco e le immagini di sfondo del desktop.</span><span class="sxs-lookup"><span data-stu-id="b22cf-109">The MDM\_Personalization class is used to set the lock screen and desktop background images.</span></span> <span data-ttu-id="b22cf-110">L'impostazione di questi criteri impedisce inoltre all'utente di modificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b22cf-110">Setting these policies also prevents the user from changing the image.</span></span>

<span data-ttu-id="b22cf-111">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b22cf-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b22cf-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b22cf-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a><span data-ttu-id="b22cf-113">Members</span><span class="sxs-lookup"><span data-stu-id="b22cf-113">Members</span></span>

<span data-ttu-id="b22cf-114">La classe di **\_ personalizzazione MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b22cf-114">The **MDM\_Personalization** class has these types of members:</span></span>

-   [<span data-ttu-id="b22cf-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b22cf-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b22cf-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b22cf-116">Properties</span></span>

<span data-ttu-id="b22cf-117">La classe di **\_ personalizzazione MDM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b22cf-117">The **MDM\_Personalization** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b22cf-118">DesktopImageStatus</span><span class="sxs-lookup"><span data-stu-id="b22cf-118">DesktopImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b22cf-119">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b22cf-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b22cf-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b22cf-121">DesktopImageUrl</span><span class="sxs-lookup"><span data-stu-id="b22cf-121">DesktopImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b22cf-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b22cf-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b22cf-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b22cf-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b22cf-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b22cf-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b22cf-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b22cf-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b22cf-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b22cf-128">LockScreenImageStatus</span><span class="sxs-lookup"><span data-stu-id="b22cf-128">LockScreenImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b22cf-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b22cf-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b22cf-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b22cf-131">LockScreenImageUrl</span><span class="sxs-lookup"><span data-stu-id="b22cf-131">LockScreenImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b22cf-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b22cf-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b22cf-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b22cf-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b22cf-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b22cf-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b22cf-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b22cf-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b22cf-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b22cf-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b22cf-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b22cf-138">Requirements</span></span>



| <span data-ttu-id="b22cf-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b22cf-139">Requirement</span></span> | <span data-ttu-id="b22cf-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b22cf-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b22cf-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b22cf-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b22cf-142">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b22cf-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b22cf-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b22cf-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b22cf-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b22cf-144">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b22cf-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b22cf-145">Namespace</span></span><br/>                | <span data-ttu-id="b22cf-146">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b22cf-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b22cf-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b22cf-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b22cf-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b22cf-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b22cf-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b22cf-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b22cf-150"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b22cf-150"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 


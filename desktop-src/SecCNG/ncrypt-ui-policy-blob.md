---
description: Utilizzato con la \_ proprietà della proprietà dei criteri dell'interfaccia utente NCRYPT \_ \_ per contenere informazioni sull'interfaccia utente per una chiave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Struttura NCRYPT_UI_POLICY_BLOB ( \_ provider NCRYPT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528728"
---
# <a name="ncrypt_ui_policy_blob-structure"></a><span data-ttu-id="53d49-103">\_ \_ Struttura BLOB dei criteri dell'interfaccia utente di NCRYPT \_</span><span class="sxs-lookup"><span data-stu-id="53d49-103">NCRYPT\_UI\_POLICY\_BLOB structure</span></span>

<span data-ttu-id="53d49-104">La struttura del **\_ \_ \_ BLOB dei criteri** dell'interfaccia utente di NCRYPT viene usata con la proprietà della [**\_ \_ \_ proprietà dei criteri**](key-storage-property-identifiers.md) dell'interfaccia utente NCRYPT per contenere informazioni sull'interfaccia utente per una chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-104">The **NCRYPT\_UI\_POLICY\_BLOB** structure is used with the [**NCRYPT\_UI\_POLICY\_PROPERTY**](key-storage-property-identifiers.md) property to contain user interface information for a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d49-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53d49-105">Syntax</span></span>


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a><span data-ttu-id="53d49-106">Members</span><span class="sxs-lookup"><span data-stu-id="53d49-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53d49-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="53d49-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="53d49-108">Numero di versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="53d49-108">The version number of the structure.</span></span> <span data-ttu-id="53d49-109">Questo membro deve contenere 1.</span><span class="sxs-lookup"><span data-stu-id="53d49-109">This member must contain 1.</span></span>

</dd> <dt>

<span data-ttu-id="53d49-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="53d49-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="53d49-111">Set di flag che forniscono informazioni o requisiti aggiuntivi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="53d49-111">A set of flags that provide additional user interface information or requirements.</span></span>



| <span data-ttu-id="53d49-112">Valore</span><span class="sxs-lookup"><span data-stu-id="53d49-112">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="53d49-113">Significato</span><span class="sxs-lookup"><span data-stu-id="53d49-113">Meaning</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <span data-ttu-id="53d49-114"><dt>**NCRYPT \_ \_ \_ \_ Flag chiave di protezione interfaccia utente**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="53d49-114"><dt>**NCRYPT\_UI\_PROTECT\_KEY\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="53d49-115">Visualizzare l'interfaccia utente chiave avanzata in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="53d49-115">Display the strong key user interface as needed.</span></span><br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <span data-ttu-id="53d49-116"><dt>**NCRYPT \_ Interfaccia utente-0x00000002 \_ \_ \_ \_ flag di protezione elevata**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="53d49-116"><dt>**NCRYPT\_UI\_FORCE\_HIGH\_PROTECTION\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="53d49-117">Forza la protezione elevata.</span><span class="sxs-lookup"><span data-stu-id="53d49-117">Force high protection.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="53d49-118">**cbCreationTitle**</span><span class="sxs-lookup"><span data-stu-id="53d49-118">**cbCreationTitle**</span></span>
</dt> <dd>

<span data-ttu-id="53d49-119">Lunghezza, in byte, del titolo di creazione.</span><span class="sxs-lookup"><span data-stu-id="53d49-119">The length, in bytes, of the creation title.</span></span> <span data-ttu-id="53d49-120">Il titolo della creazione è una stringa Unicode con terminazione null che specifica il testo usato come titolo della finestra di dialogo chiave complessa al termine della chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-120">The creation title is a null-terminated Unicode string that specifies the text that is used as the title of the strong key dialog box when the key is completed.</span></span> <span data-ttu-id="53d49-121">Il titolo di creazione deve essere inserito immediatamente dopo la struttura del **\_ \_ \_ BLOB dei criteri dell'interfaccia utente di NCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="53d49-121">The creation title must be placed immediately following the **NCRYPT\_UI\_POLICY\_BLOB** structure.</span></span> <span data-ttu-id="53d49-122">Se il valore del membro **cbCreationTitle** è impostato su 0, per il titolo della finestra di dialogo chiave complessa viene utilizzato un titolo di creazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="53d49-122">If the value of the **cbCreationTitle** member is set to 0, a default creation title is used for the title of the strong key dialog box.</span></span> <span data-ttu-id="53d49-123">Questo membro viene utilizzato solo alla finalizzazione della chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-123">This member is only used on key finalization.</span></span>

</dd> <dt>

<span data-ttu-id="53d49-124">**cbFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="53d49-124">**cbFriendlyName**</span></span>
</dt> <dd>

<span data-ttu-id="53d49-125">Lunghezza, in byte, del nome descrittivo della chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-125">The length, in bytes, of the friendly name of the key.</span></span> <span data-ttu-id="53d49-126">Il nome descrittivo è una stringa Unicode con terminazione null che contiene il testo visualizzato nella finestra di dialogo chiave complessa come nome della chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-126">The friendly name is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the name of the key.</span></span> <span data-ttu-id="53d49-127">Il nome descrittivo deve essere inserito immediatamente dopo il titolo di creazione in questo BLOB.</span><span class="sxs-lookup"><span data-stu-id="53d49-127">The friendly name must be placed immediately following the creation title in this BLOB.</span></span> <span data-ttu-id="53d49-128">Se il valore del membro **cbFriendlyName** è impostato su 0, nella finestra di dialogo chiave complessa viene utilizzato un nome predefinito.</span><span class="sxs-lookup"><span data-stu-id="53d49-128">If the value of the **cbFriendlyName** member is set to 0, a default name is used in the strong key dialog box.</span></span> <span data-ttu-id="53d49-129">Questo membro viene utilizzato sia quando la chiave viene completata sia quando viene utilizzata la chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-129">This member is used both when the key is completed and when the key is used.</span></span>

</dd> <dt>

<span data-ttu-id="53d49-130">**cbDescription**</span><span class="sxs-lookup"><span data-stu-id="53d49-130">**cbDescription**</span></span>
</dt> <dd>

<span data-ttu-id="53d49-131">Lunghezza, in byte, della descrizione della chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-131">The length, in bytes, of the key description.</span></span> <span data-ttu-id="53d49-132">La descrizione della chiave è una stringa Unicode con terminazione null che contiene il testo visualizzato nella finestra di dialogo chiave complessa come descrizione della chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-132">The key description is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the description of the key.</span></span> <span data-ttu-id="53d49-133">Il valore della descrizione deve essere inserito immediatamente dopo il nome descrittivo in questo BLOB.</span><span class="sxs-lookup"><span data-stu-id="53d49-133">The description value must be placed immediately following the friendly name in this BLOB.</span></span> <span data-ttu-id="53d49-134">Se il valore del membro **cbDescription** è impostato su 0, nella finestra di dialogo chiave complessa viene utilizzata una descrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="53d49-134">If the value of the **cbDescription** member is set to 0, a default description is used in the strong key dialog box.</span></span> <span data-ttu-id="53d49-135">Questo membro viene utilizzato sia quando la chiave viene completata sia quando viene utilizzata la chiave.</span><span class="sxs-lookup"><span data-stu-id="53d49-135">This member is used both when the key is completed and when the key is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53d49-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="53d49-136">Remarks</span></span>

<span data-ttu-id="53d49-137">Questa struttura è inclusa nell'intestazione ncrypt \_ provider. h.</span><span class="sxs-lookup"><span data-stu-id="53d49-137">This structure is included in the Ncrypt\_provider.h header.</span></span> <span data-ttu-id="53d49-138">Per utilizzare la struttura, è necessario scaricare [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) da Microsoft Connect.</span><span class="sxs-lookup"><span data-stu-id="53d49-138">To use the structure, you must download the [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) from Microsoft Connect.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d49-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53d49-139">Requirements</span></span>



| <span data-ttu-id="53d49-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="53d49-140">Requirement</span></span> | <span data-ttu-id="53d49-141">Valore</span><span class="sxs-lookup"><span data-stu-id="53d49-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d49-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53d49-142">Minimum supported client</span></span><br/> | <span data-ttu-id="53d49-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53d49-143">Windows Vista \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53d49-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53d49-144">Minimum supported server</span></span><br/> | <span data-ttu-id="53d49-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53d49-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="53d49-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53d49-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="53d49-147"><dt>\_Provider ncrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="53d49-147"><dt>Ncrypt\_provider.h</dt></span></span> </dl> |



 


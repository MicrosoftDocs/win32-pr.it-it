---
description: Specifica un percorso di file che rappresenta una posizione di archiviazione che può essere usata dal modulo di decrittografia del contenuto per i dati specifici del contenuto.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526899"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a><span data-ttu-id="7433c-103">\_ \_ Proprietà INPRIVATESTOREPATH di MF CONTENTDECRYPTIONMODULE</span><span class="sxs-lookup"><span data-stu-id="7433c-103">MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH property</span></span>

<span data-ttu-id="7433c-104">Specifica un percorso di file che rappresenta una posizione di archiviazione che può essere usata dal modulo di decrittografia del contenuto per i dati specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7433c-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>


## <a name="data-type"></a><span data-ttu-id="7433c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7433c-105">Data type</span></span>

<span data-ttu-id="7433c-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="7433c-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7433c-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="7433c-107">Property GUID</span></span>

<span data-ttu-id="7433c-108">**MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH**</span><span class="sxs-lookup"><span data-stu-id="7433c-108">**MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="7433c-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7433c-109">Property value</span></span>

<span data-ttu-id="7433c-110">Percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può usare per i dati specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7433c-110">A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>

## <a name="remarks"></a><span data-ttu-id="7433c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7433c-111">Remarks</span></span>

<span data-ttu-id="7433c-112">L'app deve eliminare il percorso dell'archivio dopo che l'oggetto CDM è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="7433c-112">The app should delete the store location after the CDM object has been released.</span></span>

<span data-ttu-id="7433c-113">Se questa proprietà non è impostata, il sistema utilizzerà il percorso specificato con la proprietà [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) per i dati specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7433c-113">If this property isn't set, the system will use the path specified with the [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) property for content-specific data.</span></span>

<span data-ttu-id="7433c-114">Impostare questa proprietà quando si crea un CDM chiamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="7433c-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="7433c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7433c-115">Requirements</span></span>



| <span data-ttu-id="7433c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7433c-116">Requirement</span></span> | <span data-ttu-id="7433c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7433c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7433c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7433c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7433c-119">Aggiornamento di Windows 10 aprile 2020</span><span class="sxs-lookup"><span data-stu-id="7433c-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="7433c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7433c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7433c-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="7433c-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7433c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7433c-122">See also</span></span>

- [<span data-ttu-id="7433c-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7433c-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="7433c-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="7433c-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 





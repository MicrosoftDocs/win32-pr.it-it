---
description: Specifica un percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può utilizzare per l'inizializzazione.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485220"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a><span data-ttu-id="d1d98-103">\_ \_ Proprietà STOREPATH di MF CONTENTDECRYPTIONMODULE</span><span class="sxs-lookup"><span data-stu-id="d1d98-103">MF\_CONTENTDECRYPTIONMODULE\_STOREPATH property</span></span>

<span data-ttu-id="d1d98-104">Specifica un percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può utilizzare per l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="d1d98-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>


## <a name="data-type"></a><span data-ttu-id="d1d98-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d1d98-105">Data type</span></span>

<span data-ttu-id="d1d98-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="d1d98-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d1d98-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="d1d98-107">Property GUID</span></span>

<span data-ttu-id="d1d98-108">**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**</span><span class="sxs-lookup"><span data-stu-id="d1d98-108">**MF\_CONTENTDECRYPTIONMODULE\_STOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="d1d98-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d1d98-109">Property value</span></span>

<span data-ttu-id="d1d98-110">Percorso di file che rappresenta una posizione di archiviazione che il modulo CDM (Content decryption Module) può utilizzare per l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="d1d98-110">A file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1d98-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1d98-111">Remarks</span></span>

<span data-ttu-id="d1d98-112">Il percorso specificato con questa proprietà verrà usato anche per i dati specifici del contenuto se la proprietà [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) non è impostata.</span><span class="sxs-lookup"><span data-stu-id="d1d98-112">The path specified with this property will also be used for content-specific data if the [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) property isn't set.</span></span>

<span data-ttu-id="d1d98-113">Per migliorare le prestazioni COM, l'app non deve eliminare il percorso dell'archivio dopo che l'oggetto CDM è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="d1d98-113">To improve COM performance, the app should not delete the store location after the CDM object has been released.</span></span>



<span data-ttu-id="d1d98-114">Impostare questa proprietà quando si crea un CDM chiamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="d1d98-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d98-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1d98-115">Requirements</span></span>



| <span data-ttu-id="d1d98-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d98-116">Requirement</span></span> | <span data-ttu-id="d1d98-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d1d98-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d98-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1d98-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d98-119">Aggiornamento di Windows 10 aprile 2020</span><span class="sxs-lookup"><span data-stu-id="d1d98-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="d1d98-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1d98-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1d98-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1d98-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d98-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1d98-122">See also</span></span>

- [<span data-ttu-id="d1d98-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1d98-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="d1d98-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="d1d98-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 





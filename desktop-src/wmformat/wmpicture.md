---
title: WM/immagine
description: L'attributo WM/Picture contiene un'immagine relativa al contenuto.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- WM/Picture formato Windows Media
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955948"
---
# <a name="wmpicture"></a><span data-ttu-id="58641-104">WM/immagine</span><span class="sxs-lookup"><span data-stu-id="58641-104">WM/Picture</span></span>

<span data-ttu-id="58641-105">L'attributo **WM/Picture** contiene un'immagine relativa al contenuto.</span><span class="sxs-lookup"><span data-stu-id="58641-105">The **WM/Picture** attribute contains a picture related to the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="58641-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="58641-106">Global Constant</span></span>

<span data-ttu-id="58641-107">g \_ wszWMPicture</span><span class="sxs-lookup"><span data-stu-id="58641-107">g\_wszWMPicture</span></span>

## <a name="data-type"></a><span data-ttu-id="58641-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="58641-108">Data Type</span></span>

<span data-ttu-id="58641-109">[**WM \_ PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ \_ Binary di tipo WMT**)</span><span class="sxs-lookup"><span data-stu-id="58641-109">[**WM\_PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="58641-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="58641-110">Remarks</span></span>

<span data-ttu-id="58641-111">Questo attributo è compatibile con il frame ID3, APIC.</span><span class="sxs-lookup"><span data-stu-id="58641-111">This attribute is compatible with the ID3 frame, APIC.</span></span> <span data-ttu-id="58641-112">La specifica ID3 per il frame APIC stabilisce che, mentre può essere presente un numero qualsiasi di frame APIC associati a un file, solo uno può essere di tipo 1 e solo uno può essere di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="58641-112">The ID3 specification for the APIC frame stipulates that, while there may be any number of APIC frames associated with a file, only one may be of type 1 and only one may be of type 2.</span></span> <span data-ttu-id="58641-113">La specifica indica inoltre che la descrizione dell'immagine non può contenere più di 64 caratteri, ma può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="58641-113">The specification also states that the description of the picture can be no longer than 64 characters, but can be empty.</span></span>

<span data-ttu-id="58641-114">Gli attributi WM/Picture aggiunti con gli oggetti di Windows Media Format SDK non vengono convalidati automaticamente per essere conformi alle specifiche ID3.</span><span class="sxs-lookup"><span data-stu-id="58641-114">WM/Picture attributes added with the objects of the Windows Media Format SDK are not automatically validated to conform to ID3 specifications.</span></span> <span data-ttu-id="58641-115">È necessario aggiungere il codice nell'applicazione per eseguire le convalide se si desidera mantenere la compatibilità completa con ID3.</span><span class="sxs-lookup"><span data-stu-id="58641-115">You must add code in your application to perform validations if you want to maintain complete compatibility with ID3.</span></span>

## <a name="see-also"></a><span data-ttu-id="58641-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58641-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58641-117">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="58641-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="58641-118">**immagine di WM \_**</span><span class="sxs-lookup"><span data-stu-id="58641-118">**WM\_PICTURE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 





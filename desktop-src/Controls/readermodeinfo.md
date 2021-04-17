---
title: Struttura READERMODEINFO
description: Contiene informazioni necessarie per inizializzare la funzione DoReaderMode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Controlli di Windows della struttura READERMODEINFO
- Controlli Windows del puntatore alla struttura PREADERMODEINFO
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477854"
---
# <a name="readermodeinfo-structure"></a><span data-ttu-id="73adf-105">Struttura READERMODEINFO</span><span class="sxs-lookup"><span data-stu-id="73adf-105">READERMODEINFO structure</span></span>

<span data-ttu-id="73adf-106">\[**READERMODEINFO** è supportato tramite Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="73adf-106">\[**READERMODEINFO** is supported through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="73adf-107">Potrebbe non essere supportata nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="73adf-107">It might be unsupported in subsequent versions.\]</span></span>

<span data-ttu-id="73adf-108">Contiene informazioni necessarie per inizializzare la funzione [**DoReaderMode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="73adf-108">Contains information required to initialize the [**DoReaderMode**](doreadermode.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="73adf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73adf-109">Syntax</span></span>


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a><span data-ttu-id="73adf-110">Members</span><span class="sxs-lookup"><span data-stu-id="73adf-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="73adf-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="73adf-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="73adf-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="73adf-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="73adf-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="73adf-113">Required.</span></span> <span data-ttu-id="73adf-114">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="73adf-114">The size of the structure, in bytes.</span></span> <span data-ttu-id="73adf-115">Impostare questo parametro su **sizeof (READERMODE)** prima di chiamare [**DoReaderMode**](doreadermode.md).</span><span class="sxs-lookup"><span data-stu-id="73adf-115">Set this parameter to **sizeof(READERMODE)** before you call [**DoReaderMode**](doreadermode.md).</span></span>

</dd> <dt>

<span data-ttu-id="73adf-116">**HWND**</span><span class="sxs-lookup"><span data-stu-id="73adf-116">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="73adf-117">Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="73adf-117">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="73adf-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="73adf-118">Required.</span></span> <span data-ttu-id="73adf-119">Handle della finestra da utilizzare per la modalità Reader.</span><span class="sxs-lookup"><span data-stu-id="73adf-119">The handle of the window to be used for reader mode.</span></span>

</dd> <dt>

<span data-ttu-id="73adf-120">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="73adf-120">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="73adf-121">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="73adf-121">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="73adf-122">Flag che personalizzano la funzionalità della finestra modalità lettore.</span><span class="sxs-lookup"><span data-stu-id="73adf-122">Flags customizing the functionality of the reader mode window.</span></span> <span data-ttu-id="73adf-123">Questo parametro può essere 0. in caso contrario, uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="73adf-123">This parameter can be 0; otherwise, one or more of the following values.</span></span>



| <span data-ttu-id="73adf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="73adf-124">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="73adf-125">Significato</span><span class="sxs-lookup"><span data-stu-id="73adf-125">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <span data-ttu-id="73adf-126"><dt>**RMF \_**</dt> <dt>0x01</dt> ZEROCURSOR</span><span class="sxs-lookup"><span data-stu-id="73adf-126"><dt>**RMF\_ZEROCURSOR**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="73adf-127">Imposta il cursore al centro dell'area specificata nella **Repubblica popolare cinese**.</span><span class="sxs-lookup"><span data-stu-id="73adf-127">Sets the cursor in the center of the area specified in **prc**.</span></span> <span data-ttu-id="73adf-128">Se questo flag non è specificato, la posizione del cursore rimane invariata.</span><span class="sxs-lookup"><span data-stu-id="73adf-128">If this flag is not specified, the cursor position remains unchanged.</span></span><br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <span data-ttu-id="73adf-129"><dt>**RMF \_**</dt> <dt>0x02</dt> VERTICALONLY</span><span class="sxs-lookup"><span data-stu-id="73adf-129"><dt>**RMF\_VERTICALONLY**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="73adf-130">Consente solo lo scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="73adf-130">Allows only vertical scrolling.</span></span><br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <span data-ttu-id="73adf-131"><dt>**RMF \_**</dt> <dt>0x04</dt> HORIZONTALONLY</span><span class="sxs-lookup"><span data-stu-id="73adf-131"><dt>**RMF\_HORIZONTALONLY**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="73adf-132">Consente solo lo scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="73adf-132">Allows only horizontal scrolling.</span></span><br/>                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="73adf-133">**PRC**</span><span class="sxs-lookup"><span data-stu-id="73adf-133">**prc**</span></span>
</dt> <dd>

<span data-ttu-id="73adf-134">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="73adf-134">Type: **LPRECT**</span></span>

</dd> <dd>

<span data-ttu-id="73adf-135">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica l'area di scorrimento nella finestra modalità lettore.</span><span class="sxs-lookup"><span data-stu-id="73adf-135">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the scrolling area in the reader mode window.</span></span> <span data-ttu-id="73adf-136">Se questo membro è **null**, viene utilizzata l'intera finestra come area di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="73adf-136">If this member is **NULL**, then the entire window is used as the scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="73adf-137">**pfnScroll**</span><span class="sxs-lookup"><span data-stu-id="73adf-137">**pfnScroll**</span></span>
</dt> <dd>

<span data-ttu-id="73adf-138">Tipo: **PFNREADERSCROLL**</span><span class="sxs-lookup"><span data-stu-id="73adf-138">Type: **PFNREADERSCROLL**</span></span>

</dd> <dd>

<span data-ttu-id="73adf-139">Puntatore a una funzione di callback [*ReaderScroll*](readerscroll.md) definita dall'applicazione utilizzata per notificare all'applicazione che è necessario scorrere la finestra in una direzione specifica.</span><span class="sxs-lookup"><span data-stu-id="73adf-139">A pointer to an application-defined [*ReaderScroll*](readerscroll.md) callback function used to notify the application that the window needs to be scrolled in a particular direction.</span></span>

</dd> <dt>

<span data-ttu-id="73adf-140">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="73adf-140">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="73adf-141">Tipo: **PFNREADERTRANSLATEDISPATCH**</span><span class="sxs-lookup"><span data-stu-id="73adf-141">Type: **PFNREADERTRANSLATEDISPATCH**</span></span>

</dd> <dd>

<span data-ttu-id="73adf-142">Puntatore a una funzione di callback [*TranslateDispatch*](translatedispatch.md) definita dall'applicazione utilizzata per ottenere la prima notifica di tutti i messaggi inviati alla finestra modalità lettore.</span><span class="sxs-lookup"><span data-stu-id="73adf-142">A pointer to an application-defined [*TranslateDispatch*](translatedispatch.md) callback function used to get first notification of any messages sent to the reader mode window.</span></span>

</dd> <dt>

<span data-ttu-id="73adf-143">**lParam**</span><span class="sxs-lookup"><span data-stu-id="73adf-143">**lParam**</span></span>
</dt> <dd>

<span data-ttu-id="73adf-144">Tipo: **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="73adf-144">Type: **[**LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="73adf-145">Informazioni aggiuntive necessarie per l'applicazione, lette dal chiamante nella funzione di callback [*ReaderScroll*](readerscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="73adf-145">Additional information as needed by the application, read by the caller in the [*ReaderScroll*](readerscroll.md) callback function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73adf-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="73adf-146">Remarks</span></span>

<span data-ttu-id="73adf-147">Questa struttura non è dichiarata in alcuna intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="73adf-147">This structure is not declared in any public header.</span></span> <span data-ttu-id="73adf-148">Per usarlo, è necessario includere la dichiarazione illustrata in precedenza nella propria intestazione.</span><span class="sxs-lookup"><span data-stu-id="73adf-148">To use it, you must include the declaration shown above in your own header.</span></span>

## <a name="requirements"></a><span data-ttu-id="73adf-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73adf-149">Requirements</span></span>



| <span data-ttu-id="73adf-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="73adf-150">Requirement</span></span> | <span data-ttu-id="73adf-151">Valore</span><span class="sxs-lookup"><span data-stu-id="73adf-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="73adf-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73adf-152">Minimum supported client</span></span><br/> | <span data-ttu-id="73adf-153">Windows Vista, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73adf-153">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="73adf-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73adf-154">Minimum supported server</span></span><br/> | <span data-ttu-id="73adf-155">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73adf-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 


---
title: Stili estesi del controllo ComboBoxEx (CommCtrl.h)
description: Supporta gli stili estesi elencati in questa sezione e la maggior parte degli stili di controllo casella combinata standard.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966d259cf427bcc83e9a8b2fb65670a2a05b9458
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387657"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="39487-103">Stili estesi del controllo ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="39487-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="39487-104">Supporta gli stili estesi elencati in questa sezione e la maggior parte degli stili di controllo casella combinata standard.</span><span class="sxs-lookup"><span data-stu-id="39487-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="39487-105">Costante</span><span class="sxs-lookup"><span data-stu-id="39487-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="39487-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39487-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="39487-107"><dt>**CBES \_ EX \_ CASESENSITIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="39487-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="39487-108">**Per le ricerche BSTR** nell'elenco verrà effettuata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="39487-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="39487-109">Sono incluse le ricerche in seguito alla digitazione di testo nella casella di modifica e nel messaggio CB \_ FINDSTRINGEXACT.</span><span class="sxs-lookup"><span data-stu-id="39487-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="39487-110"><dt>**CBES \_ EX \_ NOEDITIMAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="39487-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="39487-111">La casella di modifica e l'elenco a discesa non visualizzano le immagini degli elementi.</span><span class="sxs-lookup"><span data-stu-id="39487-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="39487-112"><dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt></span><span class="sxs-lookup"><span data-stu-id="39487-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="39487-113">La casella di modifica e l'elenco a discesa non visualizzano le immagini degli elementi.</span><span class="sxs-lookup"><span data-stu-id="39487-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="39487-114"><dt>**CBES \_ EX \_ NOSIZELIMIT**</dt></span><span class="sxs-lookup"><span data-stu-id="39487-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="39487-115">Consente di ridimensionare verticalmente il controllo ComboBoxEx rispetto al relativo controllo casella combinata contenuto.</span><span class="sxs-lookup"><span data-stu-id="39487-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="39487-116">Se le dimensioni di ComboBoxEx sono inferiori a quelle della casella combinata, la casella combinata verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="39487-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="39487-117"><dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt></span><span class="sxs-lookup"><span data-stu-id="39487-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="39487-118">Windows NT solo.</span><span class="sxs-lookup"><span data-stu-id="39487-118">Windows NT only.</span></span> <span data-ttu-id="39487-119">Nella casella di modifica verranno utilizzati i caratteri barra (/), barra rovesciata ( \\ ) e punto (.) come delimitatori di parole.</span><span class="sxs-lookup"><span data-stu-id="39487-119">The edit box will use the slash (/), backslash (\\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="39487-120">In questo modo i tasti di scelta rapida per lo spostamento del cursore parola per parola sono efficaci nei nomi di percorso e negli URL.</span><span class="sxs-lookup"><span data-stu-id="39487-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="39487-121"><dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="39487-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="39487-122">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="39487-122">**Windows Vista and later.**</span></span> <span data-ttu-id="39487-123">Determina il troncamento degli elementi nell'elenco a discesa e nella casella di modifica (quando la casella di modifica è di sola lettura) con puntini di sospensione ("...") anziché semplicemente ritagliati dal bordo del controllo.</span><span class="sxs-lookup"><span data-stu-id="39487-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="39487-124">Ciò è utile quando il controllo deve essere impostato su una larghezza fissa, ma le voci nell'elenco possono essere lunghe.</span><span class="sxs-lookup"><span data-stu-id="39487-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="39487-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="39487-125">Remarks</span></span>

<span data-ttu-id="39487-126">È possibile impostare e recuperare gli stili estesi della casella combinata usando i messaggi [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) e [**CBEM \_ GETEXTENDEDSTYLE.**](cbem-getextendedstyle.md)</span><span class="sxs-lookup"><span data-stu-id="39487-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="39487-127">Se si tenta di impostare uno stile esteso per un controllo ComboBoxEx creato con lo stile [**SIMPLE di \_ CBS,**](combo-box-styles.md) potrebbe non essere ridisegnato correttamente.</span><span class="sxs-lookup"><span data-stu-id="39487-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="39487-128">Anche **lo stile \_ SIMPLE** di CBS non funziona correttamente con lo stile esteso CBES \_ EX \_ PATHWORDBREAKPROC.</span><span class="sxs-lookup"><span data-stu-id="39487-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39487-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39487-129">Requirements</span></span>



| <span data-ttu-id="39487-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="39487-130">Requirement</span></span> | <span data-ttu-id="39487-131">Valore</span><span class="sxs-lookup"><span data-stu-id="39487-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39487-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39487-132">Header</span></span><br/> | <dl> <span data-ttu-id="39487-133"><dt>CommCtrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="39487-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






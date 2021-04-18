---
title: Stili estesi del controllo ComboBoxEx (CommCtrl. h)
description: Supportare gli stili estesi elencati in questa sezione, nonché la maggior parte degli stili standard del controllo casella combinata.
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
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327682"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="ec5cd-103">Stili estesi del controllo ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="ec5cd-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="ec5cd-104">Supportare gli stili estesi elencati in questa sezione, nonché la maggior parte degli stili standard del controllo casella combinata.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="ec5cd-105">Costante</span><span class="sxs-lookup"><span data-stu-id="ec5cd-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="ec5cd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec5cd-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="ec5cd-107"><dt>**CBES \_ ex \_ CASESENSITIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5cd-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="ec5cd-108">Per le ricerche **BSTR** nell'elenco verrà fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="ec5cd-109">Sono incluse le ricerche in seguito alla digitazione del testo nella casella di modifica e nel \_ messaggio FINDEXACTSTRING CB.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="ec5cd-110"><dt>**CBES \_ ex \_ NOEDITIMAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5cd-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="ec5cd-111">Nella casella di modifica e nell'elenco a discesa non vengono visualizzate le immagini dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="ec5cd-112"><dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5cd-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="ec5cd-113">Nella casella di modifica e nell'elenco a discesa non vengono visualizzate le immagini dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="ec5cd-114"><dt>**CBES \_ ex \_ NOSIZELIMIT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5cd-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="ec5cd-115">Consente di ridimensionare verticalmente le dimensioni del controllo ComboBoxEx rispetto al controllo casella combinata contenuto.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="ec5cd-116">Se le dimensioni del ComboBoxEx sono inferiori a quelle della casella combinata, la casella combinata verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="ec5cd-117"><dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5cd-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="ec5cd-118">Solo Windows NT.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-118">Windows NT only.</span></span> <span data-ttu-id="ec5cd-119">Nella casella di modifica vengono utilizzati i caratteri barra (/), barra rovesciata ( \) e punto (.) come delimitatori di parola.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-119">The edit box will use the slash (/), backslash (\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="ec5cd-120">In questo modo, le scelte rapide da tastiera per lo spostamento di cursore Word per parola sono valide nei nomi di percorso e negli URL.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="ec5cd-121"><dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5cd-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="ec5cd-122">**Windows Vista e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="ec5cd-122">**Windows Vista and later.**</span></span> <span data-ttu-id="ec5cd-123">Fa in modo che gli elementi nell'elenco a discesa e nella casella di modifica (quando la casella di modifica è di sola lettura) vengano troncati con i puntini di sospensione ("...") anziché semplicemente ritagliati per il bordo del controllo.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="ec5cd-124">Questa operazione è utile quando è necessario impostare il controllo su una larghezza fissa, ma le voci dell'elenco potrebbero essere lunghe.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ec5cd-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec5cd-125">Remarks</span></span>

<span data-ttu-id="ec5cd-126">È possibile impostare e recuperare gli stili estesi ComboBox usando i messaggi [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) e [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="ec5cd-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="ec5cd-127">Se si tenta di impostare uno stile esteso per un controllo ComboBoxEx creato con lo [**stile \_ semplice CBS**](combo-box-styles.md) , è possibile che non venga ridisegnato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="ec5cd-128">Lo **stile \_ semplice CBS** non funziona anche correttamente con lo \_ \_ stile esteso CBES ex PATHWORDBREAKPROC.</span><span class="sxs-lookup"><span data-stu-id="ec5cd-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec5cd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec5cd-129">Requirements</span></span>



| <span data-ttu-id="ec5cd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec5cd-130">Requirement</span></span> | <span data-ttu-id="ec5cd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ec5cd-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5cd-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec5cd-132">Header</span></span><br/> | <dl> <span data-ttu-id="ec5cd-133"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec5cd-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






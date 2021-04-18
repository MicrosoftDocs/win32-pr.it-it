---
title: Modificare gli stili estesi del controllo (CommCtrl. h)
description: Questa sezione elenca gli stili estesi usati per la creazione di controlli di modifica. Il valore degli stili estesi è una combinazione bit per bit di questi stili.
ms.assetid: 44ef7cbf-6d90-4ea0-8e23-cd84aacd5506
topic_type:
- apiref
api_name:
- ES_EX_ALLOWEOL_CR
- ES_EX_ALLOWEOL_LF
- ES_EX_ALLOWEOL_ALL
- ES_EX_CONVERT_EOL_ON_PASTE
- ES_EX_ZOOMABLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 912a13b0e05d7b12e5058435221b821b50eddf2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327244"
---
# <a name="edit-control-extended-styles"></a><span data-ttu-id="e07be-104">Modificare gli stili estesi del controllo</span><span class="sxs-lookup"><span data-stu-id="e07be-104">Edit Control Extended Styles</span></span>

<span data-ttu-id="e07be-105">Questa sezione elenca gli stili estesi usati per la creazione di controlli di modifica.</span><span class="sxs-lookup"><span data-stu-id="e07be-105">This section lists extended styles used when creating edit controls.</span></span> <span data-ttu-id="e07be-106">Il valore degli stili estesi è una combinazione bit per bit di questi stili.</span><span class="sxs-lookup"><span data-stu-id="e07be-106">The value of extended styles is a bitwise combination of these styles.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e07be-107">Costante</span><span class="sxs-lookup"><span data-stu-id="e07be-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e07be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e07be-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl> <span data-ttu-id="e07be-109"><dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e07be-109"><dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e07be-110">[Windows Vista e versioni successive](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e07be-110">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="e07be-111">Abilita il supporto per i caratteri di fine riga (CR) di ritorno a capo per le linee di interruzioni.</span><span class="sxs-lookup"><span data-stu-id="e07be-111">Enables support for carriage return (CR) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl> <span data-ttu-id="e07be-112"><dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e07be-112"><dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e07be-113">[Windows Vista e versioni successive](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e07be-113">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="e07be-114">Abilita il supporto per i caratteri di fine riga di avanzamento riga (LF) per interrompere le righe.</span><span class="sxs-lookup"><span data-stu-id="e07be-114">Enables support for linefeed (LF) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl> <span data-ttu-id="e07be-115"><dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e07be-115"><dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e07be-116">[Windows Vista e versioni successive](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e07be-116">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="e07be-117">Abilita il supporto per i caratteri di fine riga (CR) e di avanzamento riga (LF) a capo per le righe.</span><span class="sxs-lookup"><span data-stu-id="e07be-117">Enables support for both carriage return (CR) and linefeed (LF) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl> <span data-ttu-id="e07be-118"><dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e07be-118"><dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e07be-119">[Windows Vista e versioni successive](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e07be-119">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="e07be-120">Converte i caratteri di fine riga abilitati per questo controllo di modifica nel contenuto incollato in modo che corrisponda al carattere di fine riga utilizzato dal documento corrente.</span><span class="sxs-lookup"><span data-stu-id="e07be-120">Converts end-of-line characters enabled for this edit control in pasted content to match the end-of-line character used by the current document.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl> <span data-ttu-id="e07be-121"><dt><strong>ES_EX_ZOOMABLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e07be-121"><dt><strong>ES_EX_ZOOMABLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e07be-122">[Windows Vista e versioni successive](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e07be-122">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="e07be-123">Abilita lo zoom usando Ctrl + MouseWheel [**e i messaggi di zoom \_**](em-getzoom.md)em getzoom / [**\_ em**](em-setzoom.md) .</span><span class="sxs-lookup"><span data-stu-id="e07be-123">Enables zooming using Ctrl+MouseWheel and the [**EM\_GETZOOM**](em-getzoom.md)/[**EM\_SETZOOM**](em-setzoom.md) messages.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e07be-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e07be-124">Requirements</span></span>



| <span data-ttu-id="e07be-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07be-125">Requirement</span></span> | <span data-ttu-id="e07be-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e07be-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e07be-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e07be-127">Header</span></span><br/> | <dl> <span data-ttu-id="e07be-128"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e07be-128"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






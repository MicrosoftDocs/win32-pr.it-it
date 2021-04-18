---
description: La proprietà ProductLanguage specifica la lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state create nel database.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Proprietà ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330616"
---
# <a name="productlanguage-property"></a><span data-ttu-id="cbccd-103">Proprietà ProductLanguage</span><span class="sxs-lookup"><span data-stu-id="cbccd-103">ProductLanguage property</span></span>

<span data-ttu-id="cbccd-104">La proprietà **ProductLanguage** specifica la lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state create nel database.</span><span class="sxs-lookup"><span data-stu-id="cbccd-104">The **ProductLanguage** property specifies the language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="cbccd-105">Questa proprietà deve essere un identificatore di lingua numerico (LANGID).</span><span class="sxs-lookup"><span data-stu-id="cbccd-105">This property must be a numeric language identifier (LANGID).</span></span> <span data-ttu-id="cbccd-106">Se una trasformazione modifica la lingua dell'interfaccia utente nel database, deve anche modificare il valore di questa proprietà per riflettere il nuovo linguaggio.</span><span class="sxs-lookup"><span data-stu-id="cbccd-106">If a transform changes the language of the user interface in the database, then it should also change the value of this property to reflect the new language.</span></span>

<span data-ttu-id="cbccd-107">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="cbccd-107">This property is REQUIRED.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbccd-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbccd-108">Remarks</span></span>

<span data-ttu-id="cbccd-109">Il valore della proprietà **ProductLanguage** deve essere una delle lingue elencate nella proprietà di [**Riepilogo del modello**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="cbccd-109">The value of the **ProductLanguage** property must be one of the languages listed in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="cbccd-110">Quando si crea un pacchetto come indipendente dalla lingua, impostare la proprietà **ProductLanguage** su 0 e usare il tipo di carattere MS Shell Dlg come stile di testo per tutte le finestre di dialogo Create.</span><span class="sxs-lookup"><span data-stu-id="cbccd-110">When authoring a package as language-neutral, set the **ProductLanguage** property to 0 and use the MS Shell Dlg font as the text style for all authored dialogs.</span></span> <span data-ttu-id="cbccd-111">Poiché alcuni tipi di carattere non supportano tutti i set di caratteri, tramite questo tipo di carattere è possibile verificare che il testo venga visualizzato correttamente in tutte le versioni localizzate del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbccd-111">Because some fonts do not support all the character sets, by using this font you can ensure that the text is correctly displayed on all localized versions of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbccd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbccd-112">Requirements</span></span>



| <span data-ttu-id="cbccd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbccd-113">Requirement</span></span> | <span data-ttu-id="cbccd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cbccd-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbccd-115">Versione</span><span class="sxs-lookup"><span data-stu-id="cbccd-115">Version</span></span><br/> | <span data-ttu-id="cbccd-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cbccd-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cbccd-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cbccd-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cbccd-118">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cbccd-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cbccd-119">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cbccd-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbccd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbccd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbccd-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbccd-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 





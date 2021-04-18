---
description: Il metodo FormatText dell'oggetto record formatta i campi in base al modello nel campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Metodo record. FormatText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330924"
---
# <a name="recordformattext-method"></a><span data-ttu-id="aa551-103">Metodo record. FormatText</span><span class="sxs-lookup"><span data-stu-id="aa551-103">Record.FormatText method</span></span>

<span data-ttu-id="aa551-104">Il metodo **FormatText** dell'oggetto [**record**](record-object.md) formatta i campi in base al modello nel campo 0.</span><span class="sxs-lookup"><span data-stu-id="aa551-104">The **FormatText** method of the [**Record**](record-object.md) object formats fields according to the template in field 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa551-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa551-105">Syntax</span></span>


```JScript
Record.FormatText()
```



## <a name="parameters"></a><span data-ttu-id="aa551-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa551-106">Parameters</span></span>

<span data-ttu-id="aa551-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aa551-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa551-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa551-108">Return value</span></span>

<span data-ttu-id="aa551-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="aa551-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa551-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa551-110">Remarks</span></span>

<span data-ttu-id="aa551-111">Il metodo **FormatText** segue la funzionalità della funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) se a **MsiFormatRecord** è stato passato un handle di programma di installazione null come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="aa551-111">The **FormatText** method follows the functionality of the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function if **MsiFormatRecord** was passed a null installer handle as its first parameter.</span></span> <span data-ttu-id="aa551-112">Di conseguenza, vengono elaborati solo i parametri dei campi di record e le proprietà non sono disponibili per la sostituzione.</span><span class="sxs-lookup"><span data-stu-id="aa551-112">As a result, only the record field parameters are processed and properties are not available for substitution.</span></span>

<span data-ttu-id="aa551-113">Ad esempio, una stringa come "formattare questo campo: \[ 1 \] , formattare questa proprietà: \[ Property \] " viene risolta in "formattare questo campo: valore dal campo 1, formattare questa proprietà: \[ Property \] ".</span><span class="sxs-lookup"><span data-stu-id="aa551-113">For example, a string such as "format this field: \[1\], format this property: \[property\]" is resolved to "format this field: value from field 1, format this property: \[property\]."</span></span>

<span data-ttu-id="aa551-114">I parametri da [formattare](formatted.md) sono racchiusi tra parentesi quadre \[ ... \] .</span><span class="sxs-lookup"><span data-stu-id="aa551-114">Parameters that are to be [formatted](formatted.md) are enclosed in square brackets \[...\].</span></span> <span data-ttu-id="aa551-115">È possibile eseguire l'iterazione delle parentesi quadre perché le sostituzioni vengono risolte dalla parte interna.</span><span class="sxs-lookup"><span data-stu-id="aa551-115">The square brackets can be iterated because the substitutions are resolved from the inside out.</span></span>

<span data-ttu-id="aa551-116">Se una parte della stringa è racchiusa tra parentesi graffe {} e non contiene parentesi quadre, viene lasciata invariata, incluse le parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="aa551-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="aa551-117">Si noti che nel caso di [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md), **FormatText** supporta solo un set limitato di proprietà, ovvero le proprietà CustomActionData e ProductCode.</span><span class="sxs-lookup"><span data-stu-id="aa551-117">Note in the case of [deferred execution custom actions](deferred-execution-custom-actions.md), **FormatText** only supports a limited set of properties: the CustomActionData and ProductCode properties.</span></span> <span data-ttu-id="aa551-118">Per altre informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="aa551-118">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa551-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa551-119">Requirements</span></span>



| <span data-ttu-id="aa551-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa551-120">Requirement</span></span> | <span data-ttu-id="aa551-121">Valore</span><span class="sxs-lookup"><span data-stu-id="aa551-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa551-122">Versione</span><span class="sxs-lookup"><span data-stu-id="aa551-122">Version</span></span><br/> | <span data-ttu-id="aa551-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa551-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="aa551-124">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aa551-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="aa551-125">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa551-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="aa551-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aa551-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa551-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa551-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="aa551-128">IID</span><span class="sxs-lookup"><span data-stu-id="aa551-128">IID</span></span><br/>     | <span data-ttu-id="aa551-129">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="aa551-129">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="aa551-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa551-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa551-131">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="aa551-131">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[<span data-ttu-id="aa551-132">Formattato</span><span class="sxs-lookup"><span data-stu-id="aa551-132">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="aa551-133">Tipi di dati delle colonne</span><span class="sxs-lookup"><span data-stu-id="aa551-133">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 





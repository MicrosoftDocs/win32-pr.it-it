---
description: Definisce il tipo che definisce i valori validi per l'attributo Type dell'elemento Content \[ Journal Reader \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo semplice ContentTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050170"
---
# <a name="contenttypetype-simple-type"></a><span data-ttu-id="741a2-103">Tipo semplice ContentTypeType</span><span class="sxs-lookup"><span data-stu-id="741a2-103">ContentTypeType Simple Type</span></span>

<span data-ttu-id="741a2-104">Definisce il tipo che definisce i valori validi per l'attributo *Type* dell' [elemento Content \[ Journal Reader \]](content-element--journal-reader.md).</span><span class="sxs-lookup"><span data-stu-id="741a2-104">Defines the type that defines valid values for the *Type* attribute of the [Content element \[Journal Reader\]](content-element--journal-reader.md).</span></span>

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="741a2-105">Modelli</span><span class="sxs-lookup"><span data-stu-id="741a2-105">Patterns</span></span>

<span data-ttu-id="741a2-106">Il tipo semplice **ContentTypeType** è una stringa limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="741a2-106">The **ContentTypeType** simple type is a string that is restricted by the following pattern:</span></span>

-   `Normal|Inert`

## <a name="remarks"></a><span data-ttu-id="741a2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="741a2-107">Remarks</span></span>

<span data-ttu-id="741a2-108">I valori validi sono "Normal" e "inerti".</span><span class="sxs-lookup"><span data-stu-id="741a2-108">Valid values are "Normal" and "Inert".</span></span>

<span data-ttu-id="741a2-109">Se il tipo è "inerte", il contenuto contenuto è una pagina journal che rappresenta lo "sfondo" di sola lettura o non modificabile per il documento.</span><span class="sxs-lookup"><span data-stu-id="741a2-109">If the type is "Inert", then the content contained is a Journal page that is the read-only/non-editable "background" for the document.</span></span> <span data-ttu-id="741a2-110">Questo errore si verifica quando viene creato un documento utilizzando il driver della stampante Journal note writer.</span><span class="sxs-lookup"><span data-stu-id="741a2-110">This occurs when a document is created by using the Journal Note Writer printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="741a2-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="741a2-111">Requirements</span></span>



| <span data-ttu-id="741a2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="741a2-112">Requirement</span></span> | <span data-ttu-id="741a2-113">Valore</span><span class="sxs-lookup"><span data-stu-id="741a2-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="741a2-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="741a2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="741a2-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="741a2-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="741a2-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="741a2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="741a2-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="741a2-117">None supported</span></span><br/>                                     |



 

 





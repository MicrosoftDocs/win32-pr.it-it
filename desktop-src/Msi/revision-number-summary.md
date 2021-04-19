---
description: Per un pacchetto di installazione, la proprietà riepilogo Numero revisione contiene il codice del pacchetto per il pacchetto di installazione.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Proprietà riepilogo Numero revisione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332316"
---
# <a name="revision-number-summary-property"></a><span data-ttu-id="0443b-103">Proprietà riepilogo Numero revisione</span><span class="sxs-lookup"><span data-stu-id="0443b-103">Revision Number Summary property</span></span>

<span data-ttu-id="0443b-104">Per un pacchetto di installazione, la proprietà **Riepilogo numero revisione** contiene il [*codice del pacchetto*](p-gly.md) per il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="0443b-104">For an installation package, the **Revision Number Summary** property contains the [*package code*](p-gly.md) for the installer package.</span></span> <span data-ttu-id="0443b-105">Per ulteriori informazioni sui codici dei pacchetti, vedere [codici di pacchetto](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0443b-105">For more information about package codes, see [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="0443b-106">Per una trasformazione, la proprietà **Riepilogo numero revisione** elenca i GUID del codice prodotto e la versione dei prodotti nuovi e originali e il GUID del codice di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0443b-106">For a transform, the **Revision Number Summary** property lists the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="0443b-107">L'elenco è separato da punti e virgola, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0443b-107">The list is separated with semicolons as follows.</span></span>

<span data-ttu-id="0443b-108">"Originale-prodotto-codice originale-versione prodotto; New-Product codice nuovo-versione prodotto; Aggiornamento-codice "</span><span class="sxs-lookup"><span data-stu-id="0443b-108">"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"</span></span>

<span data-ttu-id="0443b-109">Per un pacchetto di patch, la proprietà **Riepilogo numero revisione** specifica il codice della patch GUID per la patch.</span><span class="sxs-lookup"><span data-stu-id="0443b-109">For a patch package, the **Revision Number Summary** property specifies the GUID patch code for the patch.</span></span> <span data-ttu-id="0443b-110">Questo può essere seguito da un elenco di GUID del codice patch per le patch obsolete che devono essere rimosse quando viene applicata questa patch.</span><span class="sxs-lookup"><span data-stu-id="0443b-110">This can be followed by a list of patch code GUIDs for obsolete patches that are to be removed when this patch is applied.</span></span> <span data-ttu-id="0443b-111">I codici patch sono concatenati senza delimitatori che separano i GUID nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0443b-111">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>

<span data-ttu-id="0443b-112">\* \* Windows Installer 3,0: \* \* se nella [tabella MsiPatchSequence](msipatchsequence-table.md)sono presenti informazioni di sequenziazione, Windows Installer 3,0 usa le informazioni di sequenziazione nella tabella e ignora l'elenco delle patch obsolete incluse nella proprietà di **Riepilogo dei numeri di revisione** .</span><span class="sxs-lookup"><span data-stu-id="0443b-112">\*\*Windows Installer 3.0:  \*\* If there is sequencing information present in the [MsiPatchSequence table](msipatchsequence-table.md), Windows Installer 3.0 uses the sequencing information in the table and ignores the list of obsolete patches included in the **Revision Number Summary** property.</span></span> <span data-ttu-id="0443b-113">Windows Installer 3,0 può comunque utilizzare le informazioni sulla patch obsolete nella proprietà **Riepilogo numero revisione** se il pacchetto non contiene una tabella MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="0443b-113">Windows Installer 3.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="0443b-114">\* \* Windows Installer 2,0: \* \* la [tabella MsiPatchSequence](msipatchsequence-table.md) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0443b-114">\*\*Windows Installer 2.0:  \*\* The [MsiPatchSequence table](msipatchsequence-table.md) is not supported.</span></span> <span data-ttu-id="0443b-115">Windows Installer 2,0 può comunque utilizzare le informazioni sulla patch obsolete nella proprietà **Riepilogo numero revisione** se il pacchetto non contiene una tabella MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="0443b-115">Windows Installer 2.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="0443b-116">Questa proprietà di riepilogo è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="0443b-116">This summary property is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="0443b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0443b-117">Requirements</span></span>



| <span data-ttu-id="0443b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0443b-118">Requirement</span></span> | <span data-ttu-id="0443b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0443b-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0443b-120">Versione</span><span class="sxs-lookup"><span data-stu-id="0443b-120">Version</span></span><br/> | <span data-ttu-id="0443b-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0443b-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0443b-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0443b-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0443b-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0443b-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0443b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0443b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0443b-125">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="0443b-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 





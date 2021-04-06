---
title: Struttura XML del file di definizione dell'interfaccia
description: Struttura XML del file di definizione dell'interfaccia
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- creazione di interfacce, file di definizione dell'interfaccia
- Interfacce di Media Player di Windows, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, struttura XML
- Struttura XML per i file di definizione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044980"
---
# <a name="skin-definition-file-xml-structure"></a><span data-ttu-id="53dc5-109">Struttura XML del file di definizione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="53dc5-109">Skin Definition File XML Structure</span></span>

<span data-ttu-id="53dc5-110">Il file di definizione dell'interfaccia è scritto in XML.</span><span class="sxs-lookup"><span data-stu-id="53dc5-110">The skin definition file is written in XML.</span></span> <span data-ttu-id="53dc5-111">Una delle principali funzionalità di XML è che è completamente strutturata ed è simile a una struttura.</span><span class="sxs-lookup"><span data-stu-id="53dc5-111">One of the important features of XML is that it is completely structured, and is similar to an outline.</span></span> <span data-ttu-id="53dc5-112">Il codice XML è semplicemente una serie di elementi, ad esempio **View** e **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="53dc5-112">The XML code is simply a series of elements such as **VIEW** and **BUTTONGROUP**.</span></span> <span data-ttu-id="53dc5-113">Si inizierà con gli elementi e quindi li si definirà con gli attributi.</span><span class="sxs-lookup"><span data-stu-id="53dc5-113">You will start with the elements and then define them with attributes.</span></span> <span data-ttu-id="53dc5-114">Nella parte restante di questa esercitazione verranno fornite informazioni dettagliate sugli attributi, ma di seguito viene illustrata la struttura degli elementi che verranno utilizzati:</span><span class="sxs-lookup"><span data-stu-id="53dc5-114">The rest of this tutorial will give you details on the attributes, but here is the outline of the elements that will be used:</span></span>


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



<span data-ttu-id="53dc5-115">Tenendo presente la semplice struttura degli elementi, è possibile avere senso degli attributi che rendono univoco ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="53dc5-115">By keeping in mind the simple structure of the elements, you can make sense of the attributes that make each element unique.</span></span> <span data-ttu-id="53dc5-116">I dettagli di ogni elemento verranno trattati negli argomenti rimanenti di questa sezione.</span><span class="sxs-lookup"><span data-stu-id="53dc5-116">Details of each element will be covered in the remaining topics of this section.</span></span> <span data-ttu-id="53dc5-117">Per ulteriori informazioni sugli elementi e sugli attributi, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="53dc5-117">For more information about elements and attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53dc5-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53dc5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53dc5-119">**Creazione del file di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="53dc5-119">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 





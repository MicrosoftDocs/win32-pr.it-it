---
description: WMI utilizza i percorsi degli oggetti nelle proprietà di riferimento delle classi di associazione per identificare gli oggetti correlati, nonché utilizzare i percorsi degli oggetti nei parametri di input o output per diversi metodi.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisiti del percorso dell'oggetto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401683"
---
# <a name="wmi-object-path-requirements"></a><span data-ttu-id="b4e7f-103">Requisiti del percorso dell'oggetto WMI</span><span class="sxs-lookup"><span data-stu-id="b4e7f-103">WMI Object Path Requirements</span></span>

<span data-ttu-id="b4e7f-104">WMI utilizza i percorsi degli oggetti nelle proprietà di riferimento delle classi di associazione per identificare gli oggetti correlati, nonché utilizzare i percorsi degli oggetti nei parametri di input o output per diversi metodi.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-104">WMI uses object paths in the reference properties of association classes to identify related objects, as well as using object paths in input or output parameters for several methods.</span></span> <span data-ttu-id="b4e7f-105">Poiché i percorsi degli oggetti vengono considerati come stringhe ai fini della ricerca e del confronto, il valore di un percorso dell'oggetto quando viene utilizzato come proprietà di riferimento è sempre la stringa stessa e non l'oggetto dereferenziato.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-105">Because object paths are treated as strings for the purpose of lookup and comparison, the value of an object path when used as a reference property is always the string itself and not the dereferenced object.</span></span> <span data-ttu-id="b4e7f-106">I confronti tra stringhe che riguardano i percorsi degli oggetti non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-106">String comparisons that deal with object paths are always case-insensitive.</span></span>

<span data-ttu-id="b4e7f-107">Un percorso dell'oggetto può utilizzare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="b4e7f-107">An object path can use the following syntax:</span></span>

-   <span data-ttu-id="b4e7f-108">Stringhe contenute tra virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-108">Strings contained in single quotation marks.</span></span>
-   <span data-ttu-id="b4e7f-109">Barra come separatore.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-109">Forward slashes as separators.</span></span>
-   <span data-ttu-id="b4e7f-110">Barre rovesciate come separatori.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-110">Backslashes as separators.</span></span>
-   <span data-ttu-id="b4e7f-111">Costanti esadecimali per numeri interi.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-111">Hexadecimal constants for integers.</span></span>
-   <span data-ttu-id="b4e7f-112">Costanti booleane per le classi con chiavi che accettano valori booleani.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-112">Boolean constants for classes with keys that take Boolean values.</span></span>
-   <span data-ttu-id="b4e7f-113">Notazione URL per rappresentare caratteri non stampabili, ad esempio %20 per uno spazio vuoto.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-113">URL notation to represent nonprinting characters, such as %20 for a blank space.</span></span>

<span data-ttu-id="b4e7f-114">Inoltre, una stringa del percorso di un oggetto deve rispettare le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4e7f-114">In addition, an object path string must obey the following restrictions:</span></span>

-   <span data-ttu-id="b4e7f-115">Un server locale utilizzato con un percorso di spazio dei nomi parziale.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-115">An assumed local server with a partial namespace path.</span></span> <span data-ttu-id="b4e7f-116">Pertanto, specificando la radice e lo spazio dei nomi predefinito sono implicati la radice e lo spazio dei nomi predefinito nel server locale.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-116">Thus, specifying the root and default namespace implies the root and default namespace on the local server.</span></span>
-   <span data-ttu-id="b4e7f-117">Nessuno spazio vuoto all'interno di un elemento o tra gli elementi.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-117">No white space either within an element or between elements.</span></span>
-   <span data-ttu-id="b4e7f-118">Le virgolette incorporate nei percorsi degli oggetti sono consentite, ma devono delimitare le virgolette con caratteri di escape, come in un'applicazione C o C++.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-118">Embedded quotation marks in object paths are allowed but must delimit the quotation mark with escape characters, as in a C or C++ application.</span></span>
-   <span data-ttu-id="b4e7f-119">Solo i valori decimali vengono riconosciuti come parti numeriche di chiavi.</span><span class="sxs-lookup"><span data-stu-id="b4e7f-119">Only decimal values are recognized as numeric portions of keys.</span></span>

 

 




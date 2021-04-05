---
description: Il codice sorgente per un'azione personalizzata di esempio denominata Launch, che soddisfa le specifiche di esempio, viene fornito dal Windows Installer SDK come file tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Creazione dell'azione personalizzata di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967259"
---
# <a name="authoring-the-launch-custom-action"></a><span data-ttu-id="70cd1-103">Creazione dell'azione personalizzata di avvio</span><span class="sxs-lookup"><span data-stu-id="70cd1-103">Authoring the Launch Custom Action</span></span>

<span data-ttu-id="70cd1-104">Il codice sorgente per un'azione personalizzata di esempio denominata Launch, che soddisfa le specifiche di esempio, viene fornito dal Windows Installer SDK come file tutorial. cpp.</span><span class="sxs-lookup"><span data-stu-id="70cd1-104">The source code for a sample custom action named Launch, which meets the sample specifications, is provided by the Windows Installer SDK as the file Tutorial.cpp.</span></span> <span data-ttu-id="70cd1-105">Questa azione personalizzata USA [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) per formattare una stringa che contiene le proprietà.</span><span class="sxs-lookup"><span data-stu-id="70cd1-105">This custom action makes use of [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) to format a string containing properties.</span></span> <span data-ttu-id="70cd1-106">La proprietà \[ \# FileKey viene \] risolta nel percorso completo del file HTML.</span><span class="sxs-lookup"><span data-stu-id="70cd1-106">The property \[\#FileKey\] resolves to the full path of the HTML file.</span></span> <span data-ttu-id="70cd1-107">Usare il file di origine per creare il file Tutorial.dll.</span><span class="sxs-lookup"><span data-stu-id="70cd1-107">Use the source file to create the file Tutorial.dll.</span></span> <span data-ttu-id="70cd1-108">Il punto di ingresso per questa DLL è LaunchTutorial.</span><span class="sxs-lookup"><span data-stu-id="70cd1-108">The entry point to this DLL is LaunchTutorial.</span></span>

<span data-ttu-id="70cd1-109">L'avvio dell'azione personalizzata di esempio chiama una DLL scritta in C++ e viene generata da un flusso binario temporaneo.</span><span class="sxs-lookup"><span data-stu-id="70cd1-109">The sample custom action Launch calls a DLL written in C++ and is generated from a temporary binary stream.</span></span> <span data-ttu-id="70cd1-110">Le azioni personalizzate di questo tipo includono le costanti del tipo di base msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData, che assegnano un tipo numerico di base uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="70cd1-110">Custom actions of this type include the base type constants msidbCustomActionTypeDll and msidbCustomActionTypeBinaryData, which give a base numeric type equal to 1.</span></span> <span data-ttu-id="70cd1-111">Vedere [azione personalizzata di tipo 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="70cd1-111">See [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="70cd1-112">Poiché le specifiche richiedono che l'installazione continui se l'azione personalizzata ha esito negativo, Launch include anche la costante facoltativa **msidbCustomActionTypeContinue**, che è 64.</span><span class="sxs-lookup"><span data-stu-id="70cd1-112">Because the specifications require that the installation continue if the custom action fails, Launch also includes the optional constant **msidbCustomActionTypeContinue**, which is 64.</span></span> <span data-ttu-id="70cd1-113">Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="70cd1-113">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span> <span data-ttu-id="70cd1-114">Il tipo numerico totale di avvio è 65.</span><span class="sxs-lookup"><span data-stu-id="70cd1-114">The total numeric type of Launch is 65.</span></span>

<span data-ttu-id="70cd1-115">Continuare ad [aggiungere Launch alle tabelle CustomAction e Binary](adding-launch-to-the-customaction-and-binary-tables.md).</span><span class="sxs-lookup"><span data-stu-id="70cd1-115">Continue to [Adding Launch to the CustomAction and Binary Tables](adding-launch-to-the-customaction-and-binary-tables.md).</span></span>

 

 




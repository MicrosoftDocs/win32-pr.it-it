---
description: Quando si dispone di un handle per un file INF, è possibile recuperare informazioni da esso in diversi modi. Funzioni quali SetupGetInfInformation, SetupQueryInfFileInformation e SetupQueryInfVersionInformation recuperano le informazioni sul file INF stesso.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Recupero di informazioni da un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312756"
---
# <a name="retrieving-information-from-an-inf-file"></a><span data-ttu-id="402c7-104">Recupero di informazioni da un file INF</span><span class="sxs-lookup"><span data-stu-id="402c7-104">Retrieving Information From an INF File</span></span>

<span data-ttu-id="402c7-105">Quando si dispone di un handle per un file INF, è possibile recuperare informazioni da esso in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="402c7-105">After you have a handle to an INF file, you can retrieve information from it in a variety of ways.</span></span> <span data-ttu-id="402c7-106">Funzioni quali [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)e [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) recuperano le informazioni sul file inf stesso.</span><span class="sxs-lookup"><span data-stu-id="402c7-106">Functions such as [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa), and [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) retrieve information about the INF file itself.</span></span>

<span data-ttu-id="402c7-107">Altre funzioni, ad esempio [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) e [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) , acquisiscono informazioni sui file di origine e le directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="402c7-107">Other functions such as [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) and [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) acquire information about the source files and target directories.</span></span>

<span data-ttu-id="402c7-108">Le funzioni di basso livello, ad esempio [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) e [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) , consentono di accedere direttamente alle informazioni archiviate in una riga o un campo di un file inf.</span><span class="sxs-lookup"><span data-stu-id="402c7-108">Low-level functions like [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) and [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) enable you to directly access information stored in a line or field of an INF file.</span></span> <span data-ttu-id="402c7-109">Queste funzioni vengono utilizzate internamente dalle funzioni di livello superiore, ma sono disponibili anche se è necessario accedere alle informazioni INF a livello di riga o di campo.</span><span class="sxs-lookup"><span data-stu-id="402c7-109">These functions are used internally by the higher-level functions, but are also available should you need to access INF information at the line or field level.</span></span>

 

 




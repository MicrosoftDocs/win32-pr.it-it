---
description: Alcuni valori utilizzati con i moduli merge configurabili richiedono una gestione del testo speciale.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Formato speciale CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226858"
---
# <a name="cmsm-special-format"></a><span data-ttu-id="2f8c1-103">Formato speciale CMSM</span><span class="sxs-lookup"><span data-stu-id="2f8c1-103">CMSM Special Format</span></span>

<span data-ttu-id="2f8c1-104">Alcuni valori utilizzati con i moduli merge configurabili richiedono una gestione del testo speciale.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-104">Certain values used with configurable merge modules require special text handling.</span></span> <span data-ttu-id="2f8c1-105">Una stringa di testo descritta come nel formato speciale "CMSM" considera il punto e virgola (;) e uguale a (=) caratteri come caratteri riservati utilizzati dallo strumento di merge client o Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-105">A text string described as being in "CMSM Special Format" treats the semicolon (;) and equals (=) characters as reserved characters used by the client merge tool or Mergemod.dll.</span></span>

<span data-ttu-id="2f8c1-106">Il formato speciale CMSM è attualmente usato nei percorsi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f8c1-106">CMSM Special format is currently used in the following locations:</span></span>

-   <span data-ttu-id="2f8c1-107">Colonna di riga della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f8c1-107">The Row column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="2f8c1-108">Colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f8c1-108">The Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="2f8c1-109">La colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md) quando bit è il valore nella colonna Format.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-109">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Bitfield is the value in the Format column.</span></span>
-   <span data-ttu-id="2f8c1-110">La colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md) quando Text è il valore nella colonna Format e enum è il valore nella colonna Type.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-110">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Text is the value in the Format column and Enum is the value in the Type column.</span></span>
-   <span data-ttu-id="2f8c1-111">La colonna DefaultValue della [tabella ModuleConfiguration](moduleconfiguration-table.md) quando Key è il valore nella colonna Format.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-111">The DefaultValue column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Key is the value in the Format column.</span></span>
-   <span data-ttu-id="2f8c1-112">Elementi configurabili nel formato chiave utilizzato dal [**Metodo ProvideTextData**](configuremodule-providetextdata.md).</span><span class="sxs-lookup"><span data-stu-id="2f8c1-112">Configurable items in the Key format used by the [**ProvideTextData method**](configuremodule-providetextdata.md).</span></span>

<span data-ttu-id="2f8c1-113">Per immettere punti e virgola letterali o caratteri uguali in un valore in formato speciale CMSM, anteporre al carattere una barra rovesciata (' \\ ').</span><span class="sxs-lookup"><span data-stu-id="2f8c1-113">To enter literal semicolons or equal characters into a value in CMSM special format, prefix the character with a backslash character ('\\').</span></span> <span data-ttu-id="2f8c1-114">Una barra rovesciata letterale può essere rappresentata da due barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-114">A literal backslash can be represented by two backslashes.</span></span> <span data-ttu-id="2f8c1-115">Un singolo carattere preceduto da una singola barra rovesciata viene convertito nel carattere singolo, anche se non è necessario l'escape del carattere.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-115">A single character prefixed by a single backslash is translated into the single character, even if escaping the character is not required.</span></span>

<span data-ttu-id="2f8c1-116">Se un carattere punto e virgola o uguale non è preceduto da una barra rovesciata, ma non ha un comportamento definito nel contesto del valore, la stringa risultante non è definita.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-116">If a semicolon or equals character is not prefixed by a backslash yet does not have a defined behavior in the context of the value, the resulting string is undefined.</span></span> <span data-ttu-id="2f8c1-117">La colonna DefaultValue della tabella ModuleConfiguration, ad esempio, è in formato speciale CMSM per tutti gli elementi chiave, perché il carattere punto e virgola è il delimitatore di colonna.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-117">For example, the DefaultValue column of the ModuleConfiguration table is in CMSM special format for all Key items because the semicolon character is the column delimiter.</span></span> <span data-ttu-id="2f8c1-118">Sebbene il carattere uguale non abbia un significato speciale in questa stringa, i caratteri letterali uguali devono comunque essere preceduti da un carattere di escape in questa stringa.</span><span class="sxs-lookup"><span data-stu-id="2f8c1-118">Although the equal character has no special meaning in this string, literal equal characters must still be escaped in this string.</span></span>

 

 




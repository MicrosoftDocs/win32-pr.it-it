---
description: Per usare le proprietà nell'installazione di, è possibile ottenere e impostare i valori delle proprietà da programmi che usano MsiGetProperty e MsiSetProperty e includere come parte di istruzioni condizionali nel database di installazione.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Recupero e impostazione delle proprietà (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882973"
---
# <a name="getting-and-setting-properties-windows-installer"></a><span data-ttu-id="cc332-103">Recupero e impostazione delle proprietà (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="cc332-103">Getting and Setting Properties (Windows Installer)</span></span>

<span data-ttu-id="cc332-104">Per usare le [Proprietà](properties.md) nell'installazione di, è possibile ottenere e impostare i valori delle proprietà da programmi che usano [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) e [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e includere come parte di istruzioni condizionali nel database di installazione.</span><span class="sxs-lookup"><span data-stu-id="cc332-104">To use [properties](properties.md) in your installation, you can get and set property values from programs using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) and [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) and include as part of conditional statements in the installation database.</span></span>

-   <span data-ttu-id="cc332-105">Per ottenere una proprietà corrente, chiamare la funzione [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="cc332-105">To obtain a current property, call the [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) function.</span></span>
-   <span data-ttu-id="cc332-106">Per ottenere lo stato di installazione corrente, chiamare la funzione [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .</span><span class="sxs-lookup"><span data-stu-id="cc332-106">To obtain the current installation state, call the [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function.</span></span>
-   <span data-ttu-id="cc332-107">Per ottenere la lingua per l'installazione corrente, chiamare la funzione [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .</span><span class="sxs-lookup"><span data-stu-id="cc332-107">To obtain the language for the current installation, call the [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) function.</span></span>
-   <span data-ttu-id="cc332-108">Per impostare una proprietà, chiamare la funzione [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="cc332-108">To set a property, call the [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) function.</span></span>
-   <span data-ttu-id="cc332-109">Per impostare lo stato di installazione, chiamare la funzione [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .</span><span class="sxs-lookup"><span data-stu-id="cc332-109">To set the installation state, call the [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) function.</span></span>
-   <span data-ttu-id="cc332-110">Per cancellare una proprietà (impostandola su null), impostare il valore della proprietà su una stringa vuota: "".</span><span class="sxs-lookup"><span data-stu-id="cc332-110">To clear a property (setting it to Null), set the property's value to an empty string: "".</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc332-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc332-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc332-112">Utilizzo delle proprietà</span><span class="sxs-lookup"><span data-stu-id="cc332-112">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="cc332-113">Impostazione dei valori delle proprietà pubbliche nella riga di comando</span><span class="sxs-lookup"><span data-stu-id="cc332-113">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="cc332-114">Cancellazione di una proprietà del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="cc332-114">Clearing an Installer Property</span></span>](clearing-an-installer-property.md)
</dt> </dl>

 

 




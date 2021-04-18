---
description: Recupero e impostazione delle informazioni sulle impostazioni locali
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recupero e impostazione delle informazioni sulle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306603"
---
# <a name="retrieving-and-setting-locale-information"></a><span data-ttu-id="a8bf3-103">Recupero e impostazione delle informazioni sulle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="a8bf3-103">Retrieving and Setting Locale Information</span></span>

<span data-ttu-id="a8bf3-104">L'applicazione deve essere in grado di recuperare e impostare informazioni specifiche sulle [impostazioni locali e le lingue](locales-and-languages.md)disponibili.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-104">The application must be able to retrieve and set specific information about available [locales and languages](locales-and-languages.md).</span></span> <span data-ttu-id="a8bf3-105">Ogni elemento delle informazioni sulle impostazioni locali, ad esempio il nome di un particolare giorno della settimana o il carattere usato come separatore decimale, presenta una costante corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-105">Each element of locale information, such as the name of a particular day of the week or the character used as a decimal separator, has a corresponding constant.</span></span> <span data-ttu-id="a8bf3-106">Le costanti disponibili sono definite in [costanti di informazioni sulle impostazioni locali](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a8bf3-106">The available constants are defined in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="a8bf3-107">L'applicazione archivia e modifica sempre le informazioni sulle impostazioni locali come una stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-107">Your application always stores and manipulates locale information as a null-terminated string.</span></span> <span data-ttu-id="a8bf3-108">Non sono consentiti dati binari e tutti i valori numerici devono essere specificati come testo.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-108">No binary data is allowed, and any numeric values must be specified as text.</span></span> <span data-ttu-id="a8bf3-109">Ogni tipo di informazioni ha un formato particolare.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-109">Each type of information has a particular format.</span></span> <span data-ttu-id="a8bf3-110">Inoltre, diversi tipi sono collegati tra loro in modo che la modifica di un tipo modifichi anche il valore dell'altro tipo.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-110">Also, several types are linked together so that changing one type changes the value of the other type as well.</span></span>

<span data-ttu-id="a8bf3-111">Per recuperare le informazioni sulle impostazioni locali, l'applicazione chiama [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante che corrisponde alle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-111">To retrieve locale information, the application calls [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with the constant that corresponds to the required information.</span></span> <span data-ttu-id="a8bf3-112">L'applicazione può chiamare [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) per impostare un elemento delle informazioni sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-112">The application can call [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) to set an item of locale information.</span></span>

> [!Note]  
> <span data-ttu-id="a8bf3-113">Sebbene sia possibile supportare un [identificatore delle impostazioni locali](locale-identifiers.md) , non è disponibile per l'utilizzo da parte di un'applicazione a meno che non vengano installate anche le impostazioni locali corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-113">Although a [locale identifier](locale-identifiers.md) might be supported, it is not available for use by an application unless the corresponding locale is also installed.</span></span>

 

<span data-ttu-id="a8bf3-114">Poiché la maggior parte delle costanti di informazioni sulle impostazioni locali si escludono a vicenda, è possibile gestire un solo tipo di informazioni alla volta.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-114">Since most locale information constants are mutually exclusive, only one type of information can be handled at a time.</span></span> <span data-ttu-id="a8bf3-115">Le eccezioni a questa regola [usano le impostazioni \_ locali \_ CP \_ ACP](locale-use-cp-acp.md), il [ \_ \_ numero restituito delle impostazioni locali](locale-return-constants.md)e le [impostazioni locali \_ NOUSEROVERRIDE](locale-nouseroverride.md), che possono essere combinate con altre costanti usando un file binario o.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-115">The exceptions to this rule are [LOCALE\_USE\_CP\_ACP](locale-use-cp-acp.md), [LOCALE\_RETURN\_NUMBER](locale-return-constants.md), and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md), which can be combined with other constants using a binary OR.</span></span>

> [!Caution]  
> <span data-ttu-id="a8bf3-116">L'uso delle impostazioni locali \_ NOUSEROVERRIDE è fortemente sconsigliato poiché Disabilita le preferenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-116">Use of LOCALE\_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</span></span>

 

<span data-ttu-id="a8bf3-117">Analogamente a una serie di applicazioni, ad esempio Microsoft Active Directory, l'applicazione è in grado di gestire le stringhe in un database ordinabile.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-117">Like a number of applications, for example Microsoft Active Directory, your application can maintain its strings in a sortable database.</span></span> <span data-ttu-id="a8bf3-118">Per ulteriori informazioni, vedere [gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a8bf3-118">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8bf3-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8bf3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8bf3-120">Uso del supporto per le lingue nazionali</span><span class="sxs-lookup"><span data-stu-id="a8bf3-120">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="a8bf3-121">Costanti di informazioni sulle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="a8bf3-121">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="a8bf3-122">Gestione dell'ordinamento nelle applicazioni</span><span class="sxs-lookup"><span data-stu-id="a8bf3-122">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="a8bf3-123">Utilizzo di impostazioni locali personalizzate</span><span class="sxs-lookup"><span data-stu-id="a8bf3-123">Working with Custom Locales</span></span>](working-with-custom-locales.md)
</dt> </dl>

 

 




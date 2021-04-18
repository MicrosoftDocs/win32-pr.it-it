---
title: Supporto IDN in WinINet
description: A partire da Windows Server 2008 e Windows Vista, la parte host dell'URL Unicode viene convertita in IDN (International Domain Name).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399588"
---
# <a name="idn-support-in-wininet"></a><span data-ttu-id="d2003-103">Supporto IDN in WinINet</span><span class="sxs-lookup"><span data-stu-id="d2003-103">IDN Support in WinINet</span></span>

<span data-ttu-id="d2003-104">A partire da Windows Server 2008 e Windows Vista, la parte host dell'URL Unicode viene convertita in IDN (International Domain Name).</span><span class="sxs-lookup"><span data-stu-id="d2003-104">Starting in Windows Server 2008 and Windows Vista, the host portion of the Unicode URL is converted to the Internationalized Domain Name (IDN).</span></span> <span data-ttu-id="d2003-105">Parti separate della codifica URL Unicode possono anche essere modificate dalle configurazioni impostate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2003-105">Separate portions of the Unicode URL encoding can also be modified by configurations set by the application.</span></span> <span data-ttu-id="d2003-106">Le versioni ANSI dell'API WinINet continuano a inviare l'URL in transito come immesso dall'applicazione, ma le versioni Unicode di WinINet dell'API sono ora conformi allo standard IDN (RFC3490) per le codifiche URL.</span><span class="sxs-lookup"><span data-stu-id="d2003-106">The ANSI versions of the WinINet API continue to send the URL over the wire as entered by the application, however the WinINet Unicode versions of the API now conform to the IDN standard (RFC3490) for URL encodings.</span></span>

<span data-ttu-id="d2003-107">Per impostazione predefinita, quando viene immesso un URL come parametro Unicode, la parte host, sia per il proxy che per le connessioni dirette, viene convertita in formato IDN.</span><span class="sxs-lookup"><span data-stu-id="d2003-107">By default, when a URL is entered as a Unicode parameter, the host portion, for both proxy and direct connections, is converted to IDN format.</span></span> <span data-ttu-id="d2003-108">Nell'applicazione è possibile disabilitare la formattazione dell'host IDN impostando l'opzione **Internet \_ option \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="d2003-108">The application has the option to disable IDN host formatting by setting the **INTERNET\_OPTION\_IDN** option.</span></span> <span data-ttu-id="d2003-109">La conversione dell'host IDN può essere abilitata solo per le connessioni dirette o proxy usando il **\_ flag Internet \_ IDN \_ Direct** o i flag del **proxy di Internet \_ flag \_ IDN \_** con l' **\_ opzione Internet \_ IDN**.</span><span class="sxs-lookup"><span data-stu-id="d2003-109">IDN host conversion can be enabled on only the direct or proxy connections by using the **INTERNET\_FLAG\_IDN\_DIRECT** or **INTERNET\_FLAG\_IDN\_PROXY** flags with **INTERNET\_OPTION\_IDN**.</span></span>

<span data-ttu-id="d2003-110">Nell'esempio di codice seguente viene illustrato come disabilitare la conversione host IDN sia per il proxy che per le connessioni dirette.</span><span class="sxs-lookup"><span data-stu-id="d2003-110">The following code example shows how to disable IDN host conversion for both the proxy and direct connections.</span></span>

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

<span data-ttu-id="d2003-111">Se la formattazione dell'host IDN è disabilitata, l'applicazione ha la possibilità di specificare la tabella codici desiderata utilizzando l' **\_ opzione Internet \_ codepage**.</span><span class="sxs-lookup"><span data-stu-id="d2003-111">If IDN host formatting is disabled, the application has the option to specify the desired codepage using **INTERNET\_OPTION\_CODEPAGE**.</span></span>

<span data-ttu-id="d2003-112">Nell'esempio di codice seguente viene illustrato come specificare la tabella codici giapponese.</span><span class="sxs-lookup"><span data-stu-id="d2003-112">The following code example shows how to specify the Japanese code page.</span></span>

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

<span data-ttu-id="d2003-113">La parte relativa al percorso dell'URL è codificata con UTF8 per impostazione predefinita e i segmenti rimanenti dell'URL, la query o il frammento, vengono convertiti nella tabella codici di sistema predefinita (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="d2003-113">The path portion of the URL is UTF8 encoded by default, and the remaining segments of the URL, the query or fragment, are converted to the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="d2003-114">Nell'esempio seguente viene illustrato come specificare la tabella codici della lingua coreana per la parte del percorso dell'URL.</span><span class="sxs-lookup"><span data-stu-id="d2003-114">The following example shows how to specify the Korean language code page for the path portion of the URL.</span></span>

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

<span data-ttu-id="d2003-115">La tabella seguente definisce le opzioni che supportano IDN.</span><span class="sxs-lookup"><span data-stu-id="d2003-115">The following table defines the options that support IDN.</span></span> <span data-ttu-id="d2003-116">Per ulteriori informazioni, vedere l'argomento [flag di opzione](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="d2003-116">For more information, see the [Option Flags](option-flags.md) topic.</span></span>



| <span data-ttu-id="d2003-117">Opzione</span><span class="sxs-lookup"><span data-stu-id="d2003-117">Option</span></span>                            | <span data-ttu-id="d2003-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2003-118">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2003-119">opzione INTERNET (tabella \_ \_ codici)</span><span class="sxs-lookup"><span data-stu-id="d2003-119">INTERNET\_OPTION\_CODEPAGE</span></span>        | <span data-ttu-id="d2003-120">Questa opzione è impostata nella richiesta o nell'handle di connessione per specificare uno schema di codifica della tabella codici per la parte host dell'URL.</span><span class="sxs-lookup"><span data-stu-id="d2003-120">This option is set on the request, or connection handle, to specify a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="d2003-121">Questa opzione viene ignorata se IDN è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d2003-121">This option is ignored if IDN is enabled.</span></span>                                                      |
| <span data-ttu-id="d2003-122">\_opzione Internet \_ percorso tabella codici \_</span><span class="sxs-lookup"><span data-stu-id="d2003-122">INTERNET\_OPTION\_CODEPAGE\_PATH</span></span>  | <span data-ttu-id="d2003-123">Questa opzione è impostata nella richiesta oppure l'handle di connessione Abilita lo schema di codifica specificato per la parte del percorso dell'URL.</span><span class="sxs-lookup"><span data-stu-id="d2003-123">This option is set on the request, or connection handle enables the specified encoding scheme for the path portion of the URL.</span></span> <span data-ttu-id="d2003-124">Per impostazione predefinita, la parte del percorso dell'URL è con codifica UTF8.</span><span class="sxs-lookup"><span data-stu-id="d2003-124">By default, the path portion of the URL is UTF8 encoded.</span></span>                                         |
| <span data-ttu-id="d2003-125">opzione INTERNET-tabella \_ \_ codici \_ aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d2003-125">INTERNET\_OPTION\_CODEPAGE\_EXTRA</span></span> | <span data-ttu-id="d2003-126">L'impostazione di questa opzione sulla richiesta o sull'handle di connessione Abilita lo schema di codifica specificato per la parte aggiuntiva dell'URL.</span><span class="sxs-lookup"><span data-stu-id="d2003-126">Setting this option on the request, or connection handle enables the specified encoding scheme for the extra portion of the URL.</span></span> <span data-ttu-id="d2003-127">Per impostazione predefinita, la parte aggiuntiva dell'URL è codificata nella tabella codici di sistema predefinita (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="d2003-127">By default, the extra portion of the URL is encoded in the default system code page (CP\_ACP).</span></span> |
| <span data-ttu-id="d2003-128">\_opzione Internet \_ IDN</span><span class="sxs-lookup"><span data-stu-id="d2003-128">INTERNET\_OPTION\_IDN</span></span>             | <span data-ttu-id="d2003-129">Questa opzione può essere utilizzata sulla richiesta o sull'handle di connessione per abilitare o disabilitare la conversione dell'host IDN.</span><span class="sxs-lookup"><span data-stu-id="d2003-129">This option can be used on the request, or connection handle to enable or disable IDN host conversion.</span></span> <span data-ttu-id="d2003-130">Quando IDN è disabilitato, WinINet usa la tabella codici di sistema predefinita per codificare la porzione host o Authority dell'URL.</span><span class="sxs-lookup"><span data-stu-id="d2003-130">When IDN is disabled, WinINet uses the default system codepage to encode the host or authority portion of the URL.</span></span>       |



 

> [!Note]  
> <span data-ttu-id="d2003-131">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="d2003-131">WinINet does not support server implementations.</span></span> <span data-ttu-id="d2003-132">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="d2003-132">In addition, it should not be used from a service.</span></span> <span data-ttu-id="d2003-133">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="d2003-133">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
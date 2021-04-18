---
title: Co-Branding negozi online
description: Co-Branding negozi online
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player Online Stores, co-branding
- negozi online, co-branding
- digitare 1 negozi online, co-branding
- digitare 2 negozi online, co-branding
- negozi online di co-branding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298213"
---
# <a name="co-branding-online-stores"></a><span data-ttu-id="dc9e7-108">Co-Branding negozi online</span><span class="sxs-lookup"><span data-stu-id="dc9e7-108">Co-Branding Online Stores</span></span>

<span data-ttu-id="dc9e7-109">I personal computer OEM che non operano in un Music Store possono coesistere con i provider di negozio online.</span><span class="sxs-lookup"><span data-stu-id="dc9e7-109">Personal computer OEMs who do not operate a music store can co-brand with online store providers.</span></span> <span data-ttu-id="dc9e7-110">Il programma di installazione di Windows Media Player supporta il parametro della riga di comando ServiceExtra per consentire agli OEM hardware di impostare un attributo personalizzato che può essere utilizzato dall'archivio online per identificare quale OEM ha installato l'archivio online iniziale.</span><span class="sxs-lookup"><span data-stu-id="dc9e7-110">Windows Media Player setup supports the ServiceExtra command line parameter to enable hardware OEMs to set a custom attribute that the online store can use to identify which OEM installed the initial online store.</span></span>

<span data-ttu-id="dc9e7-111">Ad esempio, se un produttore di computer denominato Fabrikam vuole impostare l'archivio online iniziale su Proseware Music Store, potrebbe usare la riga di comando seguente per installare Windows Media Player 10:</span><span class="sxs-lookup"><span data-stu-id="dc9e7-111">For example, if a computer maker named Fabrikam wants to set the initial online store to the Proseware music store, it might use the following command line to install Windows Media Player 10:</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



<span data-ttu-id="dc9e7-112">Quando Windows Media Player viene installato in questo modo, il lettore aggiunge la stringa ServiceExtra ogni volta che viene aperto il servizio proseware.</span><span class="sxs-lookup"><span data-stu-id="dc9e7-112">When Windows Media Player is installed in this manner, the Player appends the ServiceExtra string each time it opens the Proseware service.</span></span> <span data-ttu-id="dc9e7-113">Nell'esempio seguente viene illustrato l'URL che Windows Media Player invierà al servizio Proseware per recuperare il documento ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="dc9e7-113">The following example shows the URL that Windows Media Player would send to the Proseware service to retrieve the ServiceInfo document:</span></span>


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



<span data-ttu-id="dc9e7-114">L'archivio online di Proseware può quindi usare la stringa di query per determinare quale Windows OEM installato Media Player e restituire un documento ServiceInfo generato in modo dinamico che punti alla versione co-branding del negozio online.</span><span class="sxs-lookup"><span data-stu-id="dc9e7-114">The Proseware online store can then use the query string to determine which OEM installed Windows Media Player and return a dynamically generated ServiceInfo document that points to the co-branded version of the online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc9e7-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc9e7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc9e7-116">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="dc9e7-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="dc9e7-117">**Configurare i parametri della riga di comando per i negozi online**</span><span class="sxs-lookup"><span data-stu-id="dc9e7-117">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 





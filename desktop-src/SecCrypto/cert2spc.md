---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320979"
---
# <a name="cert2spc"></a><span data-ttu-id="5769e-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="5769e-103">Cert2SPC</span></span>

<span data-ttu-id="5769e-104">Lo strumento Cert2SPC crea un [*certificato di autore del software*](../secgloss/s-gly.md) di test usando i certificati [*X. 509*](../secgloss/x-gly.md) [](../secgloss/c-gly.md)esistenti.</span><span class="sxs-lookup"><span data-stu-id="5769e-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="5769e-105">Cert2SPC può eseguire il wrapping di più certificati X. 509 in un oggetto dati con segno [*PKCS \# 7*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5769e-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="5769e-106">Lo strumento viene installato nella \\ cartella bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5769e-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="5769e-107">Cert2SPC è disponibile come parte del Windows SDK, da cui è possibile scaricare <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="5769e-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="5769e-108">Questo strumento è solo a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="5769e-108">This tool is for test purposes only.</span></span> <span data-ttu-id="5769e-109">Un SPC valido viene ottenuto da un' [*autorità di certificazione*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5769e-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="5769e-110">**Cert2spc** *Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="5769e-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="5769e-111">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="5769e-111">*Output.spc*</span></span>

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5769e-112">*Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="5769e-112">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="5769e-113">Nomi dei certificati X. 509 da includere nel SPC.</span><span class="sxs-lookup"><span data-stu-id="5769e-113">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="5769e-114">Ogni nome di certificato termina con l'estensione cer.</span><span class="sxs-lookup"><span data-stu-id="5769e-114">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="5769e-115">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="5769e-115">*Output.spc*</span></span>            | <span data-ttu-id="5769e-116">Nome dell'oggetto PKCS \# 7 che contiene i certificati X. 509 da creare.</span><span class="sxs-lookup"><span data-stu-id="5769e-116">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="5769e-117">Il nome del file di output termina con l'estensione SPC.</span><span class="sxs-lookup"><span data-stu-id="5769e-117">The output file name ends with the .spc extension.</span></span> |



 

 

 

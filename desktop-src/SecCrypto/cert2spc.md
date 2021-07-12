---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581979"
---
# <a name="cert2spc"></a><span data-ttu-id="54f19-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="54f19-103">Cert2SPC</span></span>

<span data-ttu-id="54f19-104">Lo strumento Cert2SPC crea un certificato [*SPC (Software Publisher Certificate)*](../secgloss/s-gly.md) di test usando i [*certificati X.509*](../secgloss/x-gly.md) [*esistenti.*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="54f19-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="54f19-105">Cert2SPC può eseguire il wrapping di più certificati X.509 in un oggetto dati [*firmato PKCS \# 7.*](../secgloss/p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="54f19-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="54f19-106">Lo strumento viene installato nella cartella Bin del percorso di \\ installazione di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="54f19-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="54f19-107">Cert2SPC è disponibile come parte di Windows SDK, che è possibile scaricare da <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="54f19-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="54f19-108">Questo strumento è solo a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="54f19-108">This tool is for test purposes only.</span></span> <span data-ttu-id="54f19-109">Un SPC valido viene ottenuto da [*un'autorità di certificazione*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="54f19-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="54f19-110">**Cert2SPC** *Cert1.cer Cert2.cer* ...</span><span class="sxs-lookup"><span data-stu-id="54f19-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="54f19-111">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="54f19-111">*Output.spc*</span></span>

 



| <span data-ttu-id="54f19-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="54f19-112">Parameters</span></span>              | <span data-ttu-id="54f19-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54f19-113">Description</span></span>                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f19-114">*Cert1.cer Cert2.cer* ...</span><span class="sxs-lookup"><span data-stu-id="54f19-114">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="54f19-115">Nomi dei certificati X.509 da includere in SPC.</span><span class="sxs-lookup"><span data-stu-id="54f19-115">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="54f19-116">Ogni nome di certificato termina con l'estensione cer.</span><span class="sxs-lookup"><span data-stu-id="54f19-116">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="54f19-117">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="54f19-117">*Output.spc*</span></span>            | <span data-ttu-id="54f19-118">Nome dell'oggetto PKCS \# 7 che contiene i certificati X.509 da creare.</span><span class="sxs-lookup"><span data-stu-id="54f19-118">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="54f19-119">Il nome del file di output termina con l'estensione spc.</span><span class="sxs-lookup"><span data-stu-id="54f19-119">The output file name ends with the .spc extension.</span></span> |



 

 

 

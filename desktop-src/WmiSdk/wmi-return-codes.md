---
description: In questa sezione viene fornito un elenco dei codici restituiti WMI, delle costanti simboliche, dei valori letterali e delle descrizioni. Questi codici possono essere restituiti da script, applicazioni C++ o comandi WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Codici restituiti WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309746"
---
# <a name="wmi-return-codes"></a><span data-ttu-id="dcfb9-104">Codici restituiti WMI</span><span class="sxs-lookup"><span data-stu-id="dcfb9-104">WMI Return Codes</span></span>

<span data-ttu-id="dcfb9-105">In questa sezione viene fornito un elenco dei codici restituiti WMI, delle costanti simboliche, dei valori letterali e delle descrizioni.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-105">This section provides a list of the WMI return codes, symbolic constants, literal values, and descriptions.</span></span> <span data-ttu-id="dcfb9-106">Questi codici possono essere restituiti da script, applicazioni C++ o comandi [**wmic**](wmic.md) .</span><span class="sxs-lookup"><span data-stu-id="dcfb9-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md) commands.</span></span>

<span data-ttu-id="dcfb9-107">Se si verifica un errore, WMI restituisce uno dei codici di errore seguenti come valore a 32 bit in cui i due bit più significativi indicano il codice di gravità del messaggio.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-107">If an error occurs, WMI returns one of the following error codes as a 32-bit value where the two high-order bits indicate the severity code of the message.</span></span>

<dl> <dt>

<span data-ttu-id="dcfb9-108"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="dcfb9-108"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="dcfb9-109">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="dcfb9-109">Success</span></span>

</dd> <dt>

<span data-ttu-id="dcfb9-110"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="dcfb9-110"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="dcfb9-111">Informativo</span><span class="sxs-lookup"><span data-stu-id="dcfb9-111">Informational</span></span>

</dd> <dt>

<span data-ttu-id="dcfb9-112"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="dcfb9-112"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="dcfb9-113">Avviso</span><span class="sxs-lookup"><span data-stu-id="dcfb9-113">Warning</span></span>

</dd> <dt>

<span data-ttu-id="dcfb9-114"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="dcfb9-114"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="dcfb9-115">Errore</span><span class="sxs-lookup"><span data-stu-id="dcfb9-115">Error</span></span>

</dd> </dl>

> [!Note]
>
> <span data-ttu-id="dcfb9-116">Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-116">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="dcfb9-117">Gli errori possono provenire in altre parti del sistema operativo e emergono come errori tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-117">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="dcfb9-118">In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-118">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="dcfb9-119">Per ottenere ulteriori informazioni sull'origine del problema, è possibile scaricare ed eseguire lo strumento da riga di comando [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostica.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-119">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="dcfb9-120">Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-120">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="dcfb9-121">Il report contribuisce inoltre ai servizi di supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-121">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="dcfb9-122">È possibile scaricare il Utilità di diagnosi di WMI [qui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="dcfb9-122">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

-   [<span data-ttu-id="dcfb9-123">**Costanti di errore WMI**</span><span class="sxs-lookup"><span data-stu-id="dcfb9-123">**WMI Error Constants**</span></span>](wmi-error-constants.md)
-   [<span data-ttu-id="dcfb9-124">**Costanti non di errore WMI**</span><span class="sxs-lookup"><span data-stu-id="dcfb9-124">**WMI Non-Error Constants**</span></span>](wmi-non-error-constants.md)

 

 




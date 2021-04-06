---
description: In questo argomento viene descritto in che modo l'applicazione può specificare l'URL che lo strumento di cattura dei Tablet PC deve ottenere durante l'acquisizione dell'applicazione.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Supporto dello strumento di cattura in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883738"
---
# <a name="snipping-tool-support-in-windows-vista"></a><span data-ttu-id="2f47e-103">Supporto dello strumento di cattura in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f47e-103">Snipping Tool Support in Windows Vista</span></span>

<span data-ttu-id="2f47e-104">In questo argomento viene descritto in che modo l'applicazione può specificare l'URL che lo strumento di cattura dei Tablet PC deve ottenere durante l'acquisizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f47e-104">This topic describes how your application can specify what URL the Tablet PC Snipping Tool should obtain when capturing your application.</span></span>

## <a name="specifying-the-url-via-registry-key"></a><span data-ttu-id="2f47e-105">Specifica dell'URL tramite la chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2f47e-105">Specifying the URL via Registry Key</span></span>

<span data-ttu-id="2f47e-106">Lo strumento di cattura consente agli utenti di acquisire un oggetto snip (screenshot) di qualsiasi oggetto sullo schermo e quindi annotare, salvare o condividere l'immagine.</span><span class="sxs-lookup"><span data-stu-id="2f47e-106">Snipping Tool allows users to capture a snip (screen shot) of any object on the screen and then annotate, save, or share the image.</span></span> <span data-ttu-id="2f47e-107">Quando i dati vengono salvati in formato HTML o quando vengono inviati a un client di posta elettronica che supporta HTML inline, lo strumento di cattura può aggiungere un URL all'elemento snip se l'applicazione fornisce informazioni su come ottenere l'URL.</span><span class="sxs-lookup"><span data-stu-id="2f47e-107">When the data is saved in HTML format, or when it is sent to an email client that supports inline HTML, Snipping Tool can add a URL to the snip if the application provides information on how to obtain the URL.</span></span>

<span data-ttu-id="2f47e-108">Lo strumento di cattura Ottiene l'URL tramite oggetti di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="2f47e-108">Snipping Tool obtains the URL via accessibility objects.</span></span> <span data-ttu-id="2f47e-109">Le applicazioni devono specificare le informazioni necessarie nelle seguenti chiavi del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="2f47e-109">Applications should specify the necessary information under the following registry keys:</span></span>

<span data-ttu-id="2f47e-110">HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ lo strumento \\ di cattura LinkFingerprints,</span><span class="sxs-lookup"><span data-stu-id="2f47e-110">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints,</span></span>

<span data-ttu-id="2f47e-111">E devono creare una sottochiave il cui nome corrisponda alla classe della finestra da cui deve essere ottenuto il collegamento.</span><span class="sxs-lookup"><span data-stu-id="2f47e-111">And should create a subkey whose name is the same as the window class from which the link should be obtained.</span></span> <span data-ttu-id="2f47e-112">Il nome della classe della finestra deve essere la finestra in primo piano dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f47e-112">The window class name should be the topmost window of the application.</span></span>

<span data-ttu-id="2f47e-113">HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ lo strumento di cattura \\ LinkFingerprints\\<Window Class Name></span><span class="sxs-lookup"><span data-stu-id="2f47e-113">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints\\<Window Class Name></span></span>

### <a name="window-class-key-details"></a><span data-ttu-id="2f47e-114">Dettagli chiave classe finestra</span><span class="sxs-lookup"><span data-stu-id="2f47e-114">Window Class Key Details</span></span>

<span data-ttu-id="2f47e-115">Sotto la chiave della classe della finestra, è necessario impostare i valori appropriati per indicare che lo strumento di cattura deve rilevare l'oggetto di accessibilità corretto.</span><span class="sxs-lookup"><span data-stu-id="2f47e-115">Under the window class key, the appropriate values should be set in order to indicate Snipping Tool should detect the correct accessibility object.</span></span>



| <span data-ttu-id="2f47e-116">VALUE</span><span class="sxs-lookup"><span data-stu-id="2f47e-116">VALUE</span></span>                        | <span data-ttu-id="2f47e-117">TYPE</span><span class="sxs-lookup"><span data-stu-id="2f47e-117">TYPE</span></span>                  | <span data-ttu-id="2f47e-118">MASCHERA</span><span class="sxs-lookup"><span data-stu-id="2f47e-118">MASK</span></span>            | <span data-ttu-id="2f47e-119">INFORMAZIONI ARCHIVIATE</span><span class="sxs-lookup"><span data-stu-id="2f47e-119">INFORMATION STORED</span></span>                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| <span data-ttu-id="2f47e-120">Mask</span><span class="sxs-lookup"><span data-stu-id="2f47e-120">Mask</span></span><br/>              | <span data-ttu-id="2f47e-121">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2f47e-121">REG\_DWORD</span></span><br/> |                 | <span data-ttu-id="2f47e-122">Indica i campi seguenti da controllare</span><span class="sxs-lookup"><span data-stu-id="2f47e-122">Indicates which of the following fields to check</span></span><br/> |
| <span data-ttu-id="2f47e-123">Nome</span><span class="sxs-lookup"><span data-stu-id="2f47e-123">Name</span></span><br/>              | <span data-ttu-id="2f47e-124">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2f47e-124">REG\_SZ</span></span><br/>    | <span data-ttu-id="2f47e-125">0x02</span><span class="sxs-lookup"><span data-stu-id="2f47e-125">0x02</span></span><br/> | <span data-ttu-id="2f47e-126">Nome accessibilità</span><span class="sxs-lookup"><span data-stu-id="2f47e-126">Accessibility name</span></span><br/>                               |
| <span data-ttu-id="2f47e-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f47e-127">Description</span></span><br/>       | <span data-ttu-id="2f47e-128">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2f47e-128">REG\_SZ</span></span><br/>    | <span data-ttu-id="2f47e-129">0x04</span><span class="sxs-lookup"><span data-stu-id="2f47e-129">0x04</span></span><br/> | <span data-ttu-id="2f47e-130">Descrizione accessibilità</span><span class="sxs-lookup"><span data-stu-id="2f47e-130">Accessibility description</span></span><br/>                        |
| <span data-ttu-id="2f47e-131">Ruolo</span><span class="sxs-lookup"><span data-stu-id="2f47e-131">Role</span></span><br/>              | <span data-ttu-id="2f47e-132">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2f47e-132">REG\_DWORD</span></span><br/> | <span data-ttu-id="2f47e-133">0x08</span><span class="sxs-lookup"><span data-stu-id="2f47e-133">0x08</span></span><br/> | <span data-ttu-id="2f47e-134">Ruolo di accessibilità</span><span class="sxs-lookup"><span data-stu-id="2f47e-134">Accessibility role</span></span><br/>                               |
| <span data-ttu-id="2f47e-135">ParentName</span><span class="sxs-lookup"><span data-stu-id="2f47e-135">ParentName</span></span><br/>        | <span data-ttu-id="2f47e-136">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2f47e-136">REG\_SZ</span></span><br/>    | <span data-ttu-id="2f47e-137">0x10</span><span class="sxs-lookup"><span data-stu-id="2f47e-137">0x10</span></span><br/> | <span data-ttu-id="2f47e-138">Nome di accessibilità dell'elemento padre</span><span class="sxs-lookup"><span data-stu-id="2f47e-138">Accessibility name of parent</span></span><br/>                     |
| <span data-ttu-id="2f47e-139">ParentValue</span><span class="sxs-lookup"><span data-stu-id="2f47e-139">ParentValue</span></span><br/>       | <span data-ttu-id="2f47e-140">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2f47e-140">REG\_SZ</span></span><br/>    | <span data-ttu-id="2f47e-141">0x20</span><span class="sxs-lookup"><span data-stu-id="2f47e-141">0x20</span></span><br/> | <span data-ttu-id="2f47e-142">Valore di accessibilità dell'elemento padre</span><span class="sxs-lookup"><span data-stu-id="2f47e-142">Accessibility value of parent</span></span><br/>                    |
| <span data-ttu-id="2f47e-143">ParentRole</span><span class="sxs-lookup"><span data-stu-id="2f47e-143">ParentRole</span></span><br/>        | <span data-ttu-id="2f47e-144">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2f47e-144">REG\_DWORD</span></span><br/> | <span data-ttu-id="2f47e-145">0x40</span><span class="sxs-lookup"><span data-stu-id="2f47e-145">0x40</span></span><br/> | <span data-ttu-id="2f47e-146">Ruolo di accessibilità dell'elemento padre</span><span class="sxs-lookup"><span data-stu-id="2f47e-146">Accessibility role of parent</span></span><br/>                     |
| <span data-ttu-id="2f47e-147">ParentDescription</span><span class="sxs-lookup"><span data-stu-id="2f47e-147">ParentDescription</span></span><br/> | <span data-ttu-id="2f47e-148">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2f47e-148">REG\_SZ</span></span><br/>    | <span data-ttu-id="2f47e-149">0x80</span><span class="sxs-lookup"><span data-stu-id="2f47e-149">0x80</span></span><br/> | <span data-ttu-id="2f47e-150">Descrizione dell'accessibilità dell'elemento padre</span><span class="sxs-lookup"><span data-stu-id="2f47e-150">Accessibility description of parent</span></span><br/>              |



 

<span data-ttu-id="2f47e-151">Inoltre, se è impostato il valore di bit della maschera 0x1, l'URL deve essere prelevato dal nome dell'accessibilità; in caso contrario, l'URL deve essere tratto dal valore di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="2f47e-151">Additionally, if the mask bit value 0x1 is set, then the URL should be taken from the accessibility name; otherwise, the URL should be taken from the accessibility value.</span></span>

<span data-ttu-id="2f47e-152">Se l'applicazione usa stringhe localizzate per i \_ valori reg SZ precedenti, la stringa deve essere specificata come stringa indiretta usando il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="2f47e-152">If the application uses localized strings for the REG\_SZ values above, the string should be provided as an indirect string by using the following format:</span></span>

<span data-ttu-id="2f47e-153">@filename, risorsa</span><span class="sxs-lookup"><span data-stu-id="2f47e-153">@filename,resource</span></span>

<span data-ttu-id="2f47e-154">La stringa viene estratta dal file denominato, usando il valore della risorsa come localizzatore.</span><span class="sxs-lookup"><span data-stu-id="2f47e-154">The string is extracted from the file named, using the resource value as a locator.</span></span> <span data-ttu-id="2f47e-155">Se il valore della risorsa è zero o maggiore, il numero diventa l'indice della stringa nel file binario.</span><span class="sxs-lookup"><span data-stu-id="2f47e-155">If the resource value is zero or greater, the number becomes the index of the string in the binary file.</span></span> <span data-ttu-id="2f47e-156">Se il numero è negativo, diventa un identificatore di risorsa (ID).</span><span class="sxs-lookup"><span data-stu-id="2f47e-156">If the number is negative, it becomes a resource identifier (ID).</span></span>

> [!Note]  
> <span data-ttu-id="2f47e-157">Le costanti Role sono reperibili in oleacc. h nella Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2f47e-157">Role constants can be found in oleacc.h in the Windows SDK.</span></span> <span data-ttu-id="2f47e-158">I valori del registro di sistema descritti sono specifici di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f47e-158">The registry values described are specific to Windows Vista.</span></span>

 

 

 





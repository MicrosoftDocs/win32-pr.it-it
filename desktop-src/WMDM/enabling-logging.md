---
title: Abilitazione della registrazione
description: Abilitazione della registrazione
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Media Gestione dispositivi, registrazione
- Gestione dispositivi, registrazione
- applicazioni desktop, registrazione
- provider di servizi, registrazione
- Guida per programmatori, registrazione
- registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298042"
---
# <a name="enabling-logging"></a><span data-ttu-id="552fa-109">Abilitazione della registrazione</span><span class="sxs-lookup"><span data-stu-id="552fa-109">Enabling Logging</span></span>

<span data-ttu-id="552fa-110">Windows Media Gestione dispositivi fornisce un oggetto di registrazione che consente di salvare le informazioni in un file di testo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="552fa-110">Windows Media Device Manager provides a logging object that can save information to a text file at run time.</span></span> <span data-ttu-id="552fa-111">Gli sviluppatori di applicazioni e provider di servizi possono utilizzare questo oggetto per archiviare i messaggi in un file di log durante l'esecuzione dell'applicazione o del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="552fa-111">Developers of both applications and service providers can use this object to store messages in a log file while their application or service provider is running.</span></span> <span data-ttu-id="552fa-112">Questo oggetto è particolarmente utile quando si gestiscono file protetti da DRM, perché Windows Media Gestione dispositivi non consente di aggiungere un debugger a un processo che gestisce file protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="552fa-112">This object is especially useful when handling DRM-protected files, because Windows Media Device Manager will not allow you to attach a debugger to a process that is handling DRM-protected files.</span></span>

<span data-ttu-id="552fa-113">Il logger è un oggetto COM con ID di classe CLSID \_ WMDMLogger che espone un'interfaccia, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="552fa-113">The logger is a COM object with the class ID CLSID\_WMDMLogger that exposes one interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span> <span data-ttu-id="552fa-114">Per i componenti non è necessario un certificato per l'utilizzo dell'oggetto di registrazione.</span><span class="sxs-lookup"><span data-stu-id="552fa-114">Components do not need a certificate to use the logging object.</span></span>

<span data-ttu-id="552fa-115">Per impostazione predefinita, Windows Media Gestione dispositivi gestisce un file di log, indipendentemente dal fatto che un'applicazione usi **IWMDMLogger**.</span><span class="sxs-lookup"><span data-stu-id="552fa-115">By default, Windows Media Device Manager maintains a log file, regardless of whether an application uses **IWMDMLogger**.</span></span> <span data-ttu-id="552fa-116">Questo file di log è un semplice file di testo e ogni voce include una voce preceduta da un timestamp nel formato ad aaaammgghhmmss, che usa l'ora locale di 24 ore.</span><span class="sxs-lookup"><span data-stu-id="552fa-116">This log file is a simple text file, and each entry includes an entry preceded by a time stamp in the format YYYYMMDDHHMMSS, using 24-hour local time.</span></span> <span data-ttu-id="552fa-117">Windows Media Gestione dispositivi registra tutte le chiamate API, insieme a tutte le voci aggiunte chiamando messaggi **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="552fa-117">Windows Media Device Manager logs all API calls, along with any entries you add by calling **IWMDMLogger** messages.</span></span> <span data-ttu-id="552fa-118">Tutte le voci del file di log vengono accodate al file fino a quando non viene chiamato [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) oppure il file supera le dimensioni massime.</span><span class="sxs-lookup"><span data-stu-id="552fa-118">All log file entries are appended to the file until [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) is called, or the file exceeds its maximum size.</span></span> <span data-ttu-id="552fa-119">Il file viene chiuso automaticamente dopo ogni operazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="552fa-119">The file is closed automatically after each logging operation.</span></span> <span data-ttu-id="552fa-120">Lo stesso file di log viene utilizzato per le voci dell'applicazione e di sistema.</span><span class="sxs-lookup"><span data-stu-id="552fa-120">The same log file is used for application entries and system entries.</span></span>

<span data-ttu-id="552fa-121">Nei passaggi seguenti viene illustrato come utilizzare l'oggetto di registrazione:</span><span class="sxs-lookup"><span data-stu-id="552fa-121">The following steps show how to use the logging object:</span></span>

1.  <span data-ttu-id="552fa-122">Includere wmdmlog. h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="552fa-122">Include wmdmlog.h in your project.</span></span>
2.  <span data-ttu-id="552fa-123">Creare un oggetto di registrazione chiamando **CoCreateInstance**(CLSID \_ WMDMLogger) e richiedendo l'interfaccia **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="552fa-123">Create a logging object by calling **CoCreateInstance**(CLSID\_WMDMLogger) and requesting the **IWMDMLogger** interface.</span></span> <span data-ttu-id="552fa-124">Assegnare il puntatore di interfaccia a una variabile globale.</span><span class="sxs-lookup"><span data-stu-id="552fa-124">Assign the interface pointer to a global variable.</span></span>
3.  <span data-ttu-id="552fa-125">Verificare che la registrazione sia abilitata chiamando [**IWMDMLogger:: IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); in caso contrario, abilitarla chiamando [**IWMDMLogger:: Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span><span class="sxs-lookup"><span data-stu-id="552fa-125">Verify that logging is enabled by calling [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); if it is not, enable it by calling [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span></span>
4.  <span data-ttu-id="552fa-126">Specificare il nome e le dimensioni di un file di log personalizzato.</span><span class="sxs-lookup"><span data-stu-id="552fa-126">Specify a custom log file name and size.</span></span> <span data-ttu-id="552fa-127">Questa operazione viene eseguita chiamando [**IWMDMLogger:: Filelogfilename**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) e [**IWMDMLogger:: SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span><span class="sxs-lookup"><span data-stu-id="552fa-127">This is done by calling [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) and [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span></span>
5.  <span data-ttu-id="552fa-128">In corrispondenza dei punti nel codice in cui si vuole inserire una voce nel log, chiamare [**IWMDMLogger:: LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) per registrare stringhe contenenti variabili (questo metodo è simile a **wsprintf** nel modo in cui consente di formattare una stringa contenente un valore di variabile) o chiamare [**IWMDMLogger:: LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) per registrare stringhe costanti.</span><span class="sxs-lookup"><span data-stu-id="552fa-128">At points in your code where you want to make an entry in the log, call either [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) to log strings containing variables (this method is similar to **wsprintf** in the way it allows you to format a string containing a variable value), or call [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) to log constant strings.</span></span>

<span data-ttu-id="552fa-129">Per un esempio di codice, vedere le pagine di riferimento per i metodi di [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="552fa-129">For example code, see the reference pages for the methods of [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span>

## <a name="related-topics"></a><span data-ttu-id="552fa-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="552fa-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="552fa-131">**Attività comuni per le applicazioni e i provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="552fa-131">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





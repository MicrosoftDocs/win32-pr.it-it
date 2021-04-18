---
description: Microsoft XPS Document Writer (MXDW) è un driver di stampa per file che consente a un'applicazione Windows di creare file di documento XPS (XML Paper Specification) nelle versioni di Windows a partire da Windows XP con Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS Document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318362"
---
# <a name="microsoft-xps-document-writer-mxdw"></a><span data-ttu-id="ad6f0-103">Microsoft XPS Document Writer (MXDW)</span><span class="sxs-lookup"><span data-stu-id="ad6f0-103">Microsoft XPS Document Writer (MXDW)</span></span>

<span data-ttu-id="ad6f0-104">Microsoft XPS Document Writer (MXDW) è un driver di stampa per file che consente a un'applicazione Windows di creare file di documento XPS (XML Paper Specification) nelle versioni di Windows a partire da Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="ad6f0-104">The Microsoft XPS Document Writer (MXDW) is a print-to-file driver that enables a Windows application to create XML Paper Specification (XPS) document files on versions of Windows starting with Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="ad6f0-105">L'uso di MXDW consente a un'applicazione Windows di salvare il contenuto come documento XPS senza modificare il codice programma dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-105">Using the MXDW makes it possible for a Windows application to save its content as an XPS document without changing any of the application's program code.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ad6f0-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ad6f0-106">When to Use</span></span>

<span data-ttu-id="ad6f0-107">Quando si desidera creare un documento XPS da un'applicazione Windows che non è in grado di salvare il contenuto come documento XPS, è necessario selezionare il MXDW di un utente.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-107">As a user, you would select the MXDW when you want to create an XPS document from a Windows application that does not have the option to save its content as an XPS document.</span></span>

<span data-ttu-id="ad6f0-108">Gli sviluppatori di applicazioni possono consigliare MXDW agli utenti che desiderano creare documenti XPS quando l'applicazione non offre la possibilità di salvare un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-108">As an application developer, you would recommend the MXDW to users who want to create XPS documents when your application does not offer the option to save as an XPS document.</span></span> <span data-ttu-id="ad6f0-109">Per ulteriori informazioni sulla specifica del documento XML e sui documenti XPS, vedere [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) e [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="ad6f0-109">For more information on the XML Paper Specification and XPS documents, see [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) and [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

<span data-ttu-id="ad6f0-110">MXDW viene installato automaticamente in Windows Vista e nelle versioni successive di Windows e può essere scaricato e installato in Windows XP con SP2 e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-110">The MXDW is installed automatically on Windows Vista and later versions of Windows and can be downloaded and installed on Windows XP with SP2 and Windows Server 2003.</span></span>

## <a name="installation"></a><span data-ttu-id="ad6f0-111">Installazione</span><span class="sxs-lookup"><span data-stu-id="ad6f0-111">Installation</span></span>

<span data-ttu-id="ad6f0-112">In Windows Vista e nelle versioni successive di Windows, MXDW viene installato automaticamente quando viene installato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-112">On Windows Vista and later versions of Windows, the MXDW is installed automatically when the operating system is installed.</span></span>

<span data-ttu-id="ad6f0-113">**Windows XP con SP2 e Windows Server 2003**: scaricare e installare .net Framework 3,0 o XPS Essential Pack dall' [area download Microsoft](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad6f0-113">**Windows XP with SP2 and Windows Server 2003**: Download and install either .Net Framework 3.0 or the XPS Essential Pack from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>

## <a name="how-to-use"></a><span data-ttu-id="ad6f0-114">Uso</span><span class="sxs-lookup"><span data-stu-id="ad6f0-114">How to Use</span></span>

<span data-ttu-id="ad6f0-115">Quando è installato, il MXDW viene visualizzato come una coda di stampa disponibile nella finestra di dialogo Stampa presentata da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-115">When installed, the MXDW appears as an available print queue in the Print dialog box presented by an application.</span></span> <span data-ttu-id="ad6f0-116">Quando MXDW viene selezionato come stampante, all'utente viene richiesto il nome del file da creare come documento XPS che acquisisce l'output di stampa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-116">When the MXDW is selected as the printer, the user is prompted for the file name to create as the XPS Document that captures the print output of the application.</span></span>

<span data-ttu-id="ad6f0-117">Nella figura seguente viene illustrato il MXDW selezionato come stampante nella finestra di dialogo Stampa comune di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ad6f0-117">The following image shows the MXDW being selected as the printer in the Windows Vista common print dialog box.</span></span>

![immagine della finestra di dialogo stampa che mostra la selezione di Microsoft XPS Document Writer (MXDW)](images/choosingmxdwinvista.gif)

<span data-ttu-id="ad6f0-119">Gli sviluppatori di applicazioni possono personalizzare l'output di MXDW usando le [impostazioni di configurazione di MXDW](mxdw-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ad6f0-119">Application developers can customize the output of MXDW using the [MXDW configuration settings](mxdw-configuration-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad6f0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad6f0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad6f0-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="ad6f0-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="ad6f0-122">Specifiche XPS e download delle licenze</span><span class="sxs-lookup"><span data-stu-id="ad6f0-122">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

<span data-ttu-id="ad6f0-123">[Strumento di conformità isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad6f0-123">[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ad6f0-124">Impostazioni di configurazione di MXDW</span><span class="sxs-lookup"><span data-stu-id="ad6f0-124">MXDW configuration settings</span></span>](mxdw-configuration-settings.md)
</dt> </dl>

 

 

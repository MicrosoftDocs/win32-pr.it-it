---
description: In questa sezione vengono descritte le tecnologie del documento supportate da Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documenti XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96324014d00a2a9fc106347fbeafe9842dedd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318387"
---
# <a name="xps-documents"></a><span data-ttu-id="5eb6c-103">Documenti XPS</span><span class="sxs-lookup"><span data-stu-id="5eb6c-103">XPS Documents</span></span>

<span data-ttu-id="5eb6c-104">In questa sezione vengono descritte le tecnologie del documento supportate da Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="5eb6c-105">Scelta di una tecnologia per i documenti</span><span class="sxs-lookup"><span data-stu-id="5eb6c-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="5eb6c-106">Argomenti della sezione</span><span class="sxs-lookup"><span data-stu-id="5eb6c-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="5eb6c-107">Strumenti per documenti XPS</span><span class="sxs-lookup"><span data-stu-id="5eb6c-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="5eb6c-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5eb6c-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="5eb6c-109">Scelta di una tecnologia per i documenti</span><span class="sxs-lookup"><span data-stu-id="5eb6c-109">Choosing a Document Technology</span></span>

<span data-ttu-id="5eb6c-110">Microsoft fornisce diverse tecnologie per documenti per supportare un'ampia gamma di applicazioni di documenti:</span><span class="sxs-lookup"><span data-stu-id="5eb6c-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="5eb6c-111">**XPS e OpenXPS**</span><span class="sxs-lookup"><span data-stu-id="5eb6c-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="5eb6c-112">XPS e OpenXPS sono supportati in Windows 8 e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="5eb6c-113">Vedere il diagramma precedente per determinare lo scenario di utilizzo corretto per XPS e OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="5eb6c-114">Per ulteriori informazioni su queste tecnologie dei documenti, vedere la pagina relativa alla [specifica Open XML Paper (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="5eb6c-115">Nel caso di utilizzo di OpenXPS con Windows 8 e Windows Server 2012, il supporto viene fornito solo tramite l' [API del documento XPS](documents-xps.md)</span><span class="sxs-lookup"><span data-stu-id="5eb6c-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="5eb6c-116">Se è necessario eseguire la conversione tra Microsoft XPS (MSXPS) e OpenXPS, Microsoft ha fornito uno strumento (XPSConverter.exe) che consente di convertire i documenti in formato MSXPS nel formato OpenXPS e viceversa.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="5eb6c-117">Lo strumento fa parte del Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="5eb6c-118">Per scaricare WDK, vedere [come ottenere il WDK](/windows-hardware/drivers/download-the-wdk).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="5eb6c-119">Per ulteriori informazioni su OpenXPS e Windows 8, vedere [supporto di OpenXPS in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="5eb6c-120">**API documenti XPS**</span><span class="sxs-lookup"><span data-stu-id="5eb6c-120">**XPS Document API**</span></span>

    <span data-ttu-id="5eb6c-121">L'API documento XPS è un'API Windows nativa che supporta XPS OM.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="5eb6c-122">L'API documento XPS è stata introdotta in Windows 7 e può essere utilizzata nei programmi in modalità utente e nei driver della stampante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="5eb6c-123">Per ulteriori informazioni, vedere l'API Document XPS e l' [API di firma digitale XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="5eb6c-124">\*L'API documenti XPS è inoltre supportata in Windows Vista con Service Pack 2 (SP2) con l'aggiornamento della piattaforma per Windows Vista e Windows Server 2008 con SP2 mediante l'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="5eb6c-125">Per ulteriori informazioni sull'aggiornamento della piattaforma per Windows Vista o sull'aggiornamento della piattaforma per Windows Server 2008, vedere Aggiornamento della piattaforma [per Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span><span class="sxs-lookup"><span data-stu-id="5eb6c-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="5eb6c-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="5eb6c-126">**.NET Framework**</span></span>

    <span data-ttu-id="5eb6c-127">.NET Framework fornisce il supporto del documento XPS ai programmi in modalità utente e di codice gestito.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="5eb6c-128">.NET Framework 3,0 è supportato in Windows XP con Service Pack 2 (SP2) e nelle versioni successive dei sistemi operativi client Windows e in Windows Server 2003 con Service Pack 2 (SP2) e nelle versioni successive dei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="5eb6c-129">.NET Framework 3,5 è supportato nelle versioni di Windows XP dei sistemi operativi client Windows e in Windows Server 2003 e versioni successive dei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="5eb6c-130">Si consiglia di utilizzare .NET Framework per la creazione di documenti XPS solo nelle applicazioni client, non nelle applicazioni server, a meno che l'applicazione non venga chiusa periodicamente, come se si trattasse di un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="5eb6c-131">Per ulteriori informazioni sul supporto dei documenti in .NET Framework, vedere [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="5eb6c-132">Per lavorare con i documenti XPS in un programma, usare l'API documenti XPS nativa o il .NET Framework; l'utilizzo simultaneo di entrambi nello stesso programma non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="5eb6c-133">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5eb6c-133">In This Section</span></span>

<span data-ttu-id="5eb6c-134">In questa sezione vengono descritte le tecnologie native dei documenti Windows supportate da Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



|                                                                    |                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb6c-135">API documenti XPS</span><span class="sxs-lookup"><span data-stu-id="5eb6c-135">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="5eb6c-136">Fornisce un formato attendibile per la carta elettronica.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-136">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="5eb6c-137">L'API Document XPS descritta in questa sezione fornisce ai programmi e ai driver di stampa XPSDrv l'accesso al contenuto e ai metadati di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-137">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="5eb6c-138">API di firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="5eb6c-138">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="5eb6c-139">Abilita la firma del documento, la verifica dell'identità del firmatario e indica se un documento XPS è stato modificato dopo che è stato firmato.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-139">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="5eb6c-140">Glossario documenti XPS</span><span class="sxs-lookup"><span data-stu-id="5eb6c-140">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="5eb6c-141">Definizioni dei termini usati dall' [API Document XPS](documents-xps.md) e dall' [API di firma digitale XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-141">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="5eb6c-142">Strumenti per documenti XPS</span><span class="sxs-lookup"><span data-stu-id="5eb6c-142">XPS Document Tools</span></span>

<span data-ttu-id="5eb6c-143">Sono disponibili gli strumenti seguenti che consentono di testare e risolvere i problemi dei file di documento XPS.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-143">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="5eb6c-144">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="5eb6c-144">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="5eb6c-145">Verifica la conformità di un file alle specifiche XPS (XML Paper Specification) e Open Packaging Conventions (OPC).</span><span class="sxs-lookup"><span data-stu-id="5eb6c-145">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="5eb6c-146">XpsAnalyzer</span><span class="sxs-lookup"><span data-stu-id="5eb6c-146">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="5eb6c-147">Strumento del prompt dei comandi che analizza i file di documento XPS per la compatibilità con la specifica XPS 1,0.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-147">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="5eb6c-148">[PTConform](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5eb6c-148">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="5eb6c-149">Strumento che controlla la validità dei documenti PrintTicket e PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="5eb6c-149">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eb6c-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5eb6c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb6c-151">API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="5eb6c-151">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="5eb6c-152">Packaging</span><span class="sxs-lookup"><span data-stu-id="5eb6c-152">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="5eb6c-153">Stampa</span><span class="sxs-lookup"><span data-stu-id="5eb6c-153">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="5eb6c-154">[Stampa programma di esempio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="5eb6c-154">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 


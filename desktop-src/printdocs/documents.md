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
# <a name="xps-documents"></a>Documenti XPS

In questa sezione vengono descritte le tecnologie del documento supportate da Microsoft Windows.

-   [Scelta di una tecnologia per i documenti](#choosing-a-document-technology)
-   [Argomenti della sezione](#in-this-section)
-   [Strumenti per documenti XPS](#xps-document-tools)
-   [Argomenti correlati](#related-topics)


## <a name="choosing-a-document-technology"></a>Scelta di una tecnologia per i documenti

Microsoft fornisce diverse tecnologie per documenti per supportare un'ampia gamma di applicazioni di documenti:

-   **XPS e OpenXPS**

    XPS e OpenXPS sono supportati in Windows 8 e nelle versioni successive di Windows. Vedere il diagramma precedente per determinare lo scenario di utilizzo corretto per XPS e OpenXPS. Per ulteriori informazioni su queste tecnologie dei documenti, vedere la pagina relativa alla [specifica Open XML Paper (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).

    Nel caso di utilizzo di OpenXPS con Windows 8 e Windows Server 2012, il supporto viene fornito solo tramite l' [API del documento XPS](documents-xps.md)

    Se è necessario eseguire la conversione tra Microsoft XPS (MSXPS) e OpenXPS, Microsoft ha fornito uno strumento (XPSConverter.exe) che consente di convertire i documenti in formato MSXPS nel formato OpenXPS e viceversa. Lo strumento fa parte del Windows Driver Kit (WDK). Per scaricare WDK, vedere [come ottenere il WDK](/windows-hardware/drivers/download-the-wdk).

    Per ulteriori informazioni su OpenXPS e Windows 8, vedere [supporto di OpenXPS in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).

-   **API documenti XPS**

    L'API documento XPS è un'API Windows nativa che supporta XPS OM. L'API documento XPS è stata introdotta in Windows 7 e può essere utilizzata nei programmi in modalità utente e nei driver della stampante XPSDrv.

    Per ulteriori informazioni, vedere l'API Document XPS e l' [API di firma digitale XPS](xps-digital-signatures.md).

    \*L'API documenti XPS è inoltre supportata in Windows Vista con Service Pack 2 (SP2) con l'aggiornamento della piattaforma per Windows Vista e Windows Server 2008 con SP2 mediante l'aggiornamento della piattaforma per Windows Server 2008. Per ulteriori informazioni sull'aggiornamento della piattaforma per Windows Vista o sull'aggiornamento della piattaforma per Windows Server 2008, vedere Aggiornamento della piattaforma [per Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)

-   **.NET Framework**

    .NET Framework fornisce il supporto del documento XPS ai programmi in modalità utente e di codice gestito.

    .NET Framework 3,0 è supportato in Windows XP con Service Pack 2 (SP2) e nelle versioni successive dei sistemi operativi client Windows e in Windows Server 2003 con Service Pack 2 (SP2) e nelle versioni successive dei sistemi operativi Windows Server.

    .NET Framework 3,5 è supportato nelle versioni di Windows XP dei sistemi operativi client Windows e in Windows Server 2003 e versioni successive dei sistemi operativi Windows Server.

    > [!Note]  
    > Si consiglia di utilizzare .NET Framework per la creazione di documenti XPS solo nelle applicazioni client, non nelle applicazioni server, a meno che l'applicazione non venga chiusa periodicamente, come se si trattasse di un'applicazione client.

     

    Per ulteriori informazioni sul supporto dei documenti in .NET Framework, vedere [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Per lavorare con i documenti XPS in un programma, usare l'API documenti XPS nativa o il .NET Framework; l'utilizzo simultaneo di entrambi nello stesso programma non è supportato.

 

## <a name="in-this-section"></a>Contenuto della sezione

In questa sezione vengono descritte le tecnologie native dei documenti Windows supportate da Microsoft Windows.



|                                                                    |                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [API documenti XPS](documents-xps.md)<br/>                   | Fornisce un formato attendibile per la carta elettronica.<br/> L'API Document XPS descritta in questa sezione fornisce ai programmi e ai driver di stampa XPSDrv l'accesso al contenuto e ai metadati di un documento XPS.<br/> |
| [API di firma digitale XPS](xps-digital-signatures.md)<br/> | Abilita la firma del documento, la verifica dell'identità del firmatario e indica se un documento XPS è stato modificato dopo che è stato firmato.<br/>                                                                          |
| [Glossario documenti XPS](xpsapi-glossary.md)<br/>           | Definizioni dei termini usati dall' [API Document XPS](documents-xps.md) e dall' [API di firma digitale XPS](xps-digital-signatures.md).<br/>                                                                              |



 

## <a name="xps-document-tools"></a>Strumenti per documenti XPS

Sono disponibili gli strumenti seguenti che consentono di testare e risolvere i problemi dei file di documento XPS.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Verifica la conformità di un file alle specifiche XPS (XML Paper Specification) e Open Packaging Conventions (OPC).

-   [XpsAnalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    Strumento del prompt dei comandi che analizza i file di documento XPS per la compatibilità con la specifica XPS 1,0.

-   [PTConform](/previous-versions/dd327476(v=msdn.10))

    Strumento che controlla la validità dei documenti PrintTicket e PrintCapabilities.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di stampa XPS](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Stampa](./printdocs-printing.md)
</dt> <dt>
  
[Stampa programma di esempio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 


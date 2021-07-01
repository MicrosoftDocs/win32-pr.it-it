---
description: Questa sezione descrive le tecnologie dei documenti supportate da Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documenti XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119986"
---
# <a name="xps-documents"></a>Documenti XPS

Questa sezione descrive le tecnologie dei documenti supportate da Microsoft Windows.

-   [Scelta di una tecnologia dei documenti](#choosing-a-document-technology)
-   [Argomenti della sezione](#in-this-section)
-   [Strumenti documento XPS](#xps-document-tools)
-   [Argomenti correlati](#related-topics)


## <a name="choosing-a-document-technology"></a>Scelta di una tecnologia dei documenti

Microsoft offre diverse tecnologie di documenti per supportare un'ampia gamma di applicazioni di documenti:

-   **XPS e OpenXPS**

    XPS e OpenXPS sono supportati in Windows 8 e versioni successive di Windows. Vedere il diagramma precedente per determinare lo scenario di utilizzo corretto per XPS e OpenXPS. Per altre informazioni su queste tecnologie dei documenti, vedere [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).

    Nel caso dell'uso di OpenXPS con Windows 8 e Windows Server 2012, il supporto viene fornito solo tramite [l'API documento XPS](documents-xps.md)

    Se è necessario eseguire la conversione tra Microsoft XPS (MSXPS) e OpenXPS, Microsoft ha fornito uno strumento (XPSConverter.exe) che consente di convertire i documenti in formato MSXPS nel formato OpenXPS e viceversa. Lo strumento fa parte del Windows Driver Kit (WDK) (WDK). Per scaricare WDK, vedere [Come ottenere WDK.](/windows-hardware/drivers/download-the-wdk)

    Per altre informazioni su OpenXPS e Windows 8, vedere [Supporto di OpenXPS in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).

-   **API documento XPS**

    L'API documento XPS è un'API nativa di Windows che supporta xps OM. L'API documento XPS è stata introdotta in Windows 7 e può essere usata nei programmi in modalità utente e nei driver della stampante XPSDrv.

    Per altre informazioni, vedere l'API documento XPS e [l'API di firma digitale XPS](xps-digital-signatures.md).

    \*L'API documento XPS è supportata anche in Windows Vista con Service Pack 2 (SP2) con l'aggiornamento della piattaforma per Windows Vista e Windows Server 2008 con SP2 usando l'aggiornamento della piattaforma per Windows Server 2008. Per altre informazioni sull'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008, vedere [Aggiornamento della piattaforma per Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)

-   **.NET Framework**

    .NET Framework fornisce il supporto dei documenti XPS ai programmi in modalità utente e codice gestito.

    .NET Framework 3.0 è supportato in Windows XP con Service Pack 2 (SP2) e versioni successive dei sistemi operativi client Windows e in Windows Server 2003 con Service Pack 2 (SP2) e versioni successive dei sistemi operativi Windows Server.

    .NET Framework 3.5 è supportato nelle versioni windows XP dei sistemi operativi client Windows e in Windows Server 2003 e versioni successive dei sistemi operativi server Windows.

    > [!Note]  
    > È consigliabile usare .NET Framework per la creazione di documenti XPS solo nelle applicazioni client, non nelle applicazioni server, a meno che l'applicazione non venga chiusa periodicamente, come farebbe se si trattasse di un'applicazione client.

     

    Per altre informazioni sul supporto dei documenti in .NET Framework, vedere [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Per usare documenti XPS in un programma, usare l'API documento XPS nativa o l'api .NET Framework; L'uso simultaneo di entrambi nello stesso programma non è supportato.

 

## <a name="in-this-section"></a>Contenuto della sezione

In questa sezione vengono descritte le tecnologie dei documenti nativi di Windows supportate da Microsoft Windows.



| Tecnologia dei documenti                                                                   | Descrizione                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [API documento XPS](documents-xps.md)<br/>                   | Fornisce un formato attendibile per la carta elettronica.<br/> L'API documento XPS descritta in questa sezione consente ai programmi e ai driver di stampa XPSDrv di accedere al contenuto e ai metadati di un documento XPS.<br/> |
| [API di firma digitale XPS](xps-digital-signatures.md)<br/> | Consente la firma dei documenti, la verifica dell'identità del firmatario e l'indicazione se un documento XPS è stato modificato dopo la firma.<br/>                                                                          |
| [Glossario dei documenti XPS](xpsapi-glossary.md)<br/>           | Definizioni dei termini usati [dall'API Documento XPS](documents-xps.md) e dall'API firma digitale [XPS](xps-digital-signatures.md).<br/>                                                                              |



 

## <a name="xps-document-tools"></a>Strumenti documento XPS

Sono disponibili gli strumenti seguenti per facilitare il test e la risoluzione dei problemi dei file di documento XPS.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Verifica la conformità di un file alla XML Paper Specification (XPS) e alla specifica Open Packaging Conventions (OPC).

-   [XpsAnalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    Strumento del prompt dei comandi che analizza i file di documento XPS per verificarne la compatibilità con la specifica XPS 1.0.

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
  
[Programma di esempio per la stampa](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 


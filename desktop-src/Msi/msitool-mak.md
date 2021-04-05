---
description: MSITool. MAK è un makefile che è possibile usare per compilare strumenti e azioni personalizzate.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: MSITool. MAK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131307"
---
# <a name="msitoolmak"></a>MSITool. MAK

MSITool. MAK è un makefile che è possibile usare per compilare strumenti e azioni personalizzate. Può essere usato con Visual C++ versione 4,0 o successiva. Per ulteriori informazioni, vedere il file di intestazione. È necessario definire un set di valori prima di includere questo file. In genere, gli sviluppatori li inseriscono all'inizio di. cpp, ifdef deve essere ignorato dal compilatore C. Allo stesso modo, le risorse vengono aggiunte alla fine del file con estensione cpp. Per informazioni dettagliate, vedere esempi.

VCBIN può essere definito nella directory in cui vengono trovati gli strumenti di Visual C++ o il makefile USA MSVCDIR e MSDEVDIR. Se non sono definiti, non specifica un percorso, supponendo che gli strumenti si trovino nel percorso. Un problema con le variabili di ambiente in Visual C++ versione 5,0 è che se non sono presenti entrambi i percorsi, il linker non è in grado di trovare Msdis100.dll. Se lo si copia da MSDEVDIR a MSVCDIR, funziona. L'altra opzione consiste nel copiare Msdis100.dll e Rc.exe e Rcdll.dll in MSVCDIR e impostare VCBIN su tale.

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




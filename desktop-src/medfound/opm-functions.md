---
description: Le funzioni seguenti vengono utilizzate con l'output Protection Manager (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Funzioni di OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309065"
---
# <a name="opm-functions"></a>Funzioni di OPM

Le funzioni seguenti vengono utilizzate con l' [Output Protection Manager](output-protection-manager.md) (OPM).



| Funzione                                                                                             | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**OPMGetVideoOutputForTarget**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | Restituisce un oggetto di output video per la destinazione VidPN sull'adapter specificato.                                                          |
| [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | Crea un oggetto di gestione della protezione di output (OPM) per ogni monitoraggio fisico associato a un particolare handle **HMONITOR** . |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | Crea un oggetto OPM per ogni monitoraggio fisico associato a un particolare dispositivo Direct3D.                                 |



 

Le funzioni seguenti vengono usate da OPM per accedere alla funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare queste funzioni.

-   [**ConfigureOPMProtectedOutput**](configureopmprotectedoutput.md)
-   [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)
-   [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md)
-   [**GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [**GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [**GetCOPPCompatibleOPMInformation**](getcoppcompatibleopminformation.md)
-   [**GetOPMInformation**](getopminformation.md)
-   [**GetOPMRandomNumber**](getopmrandomnumber.md)
-   [**GetSuggestedOPMProtectedOutputArraySize**](getsuggestedopmprotectedoutputarraysize.md)
-   [**SetOPMSigningKeyAndSequenceNumbers**](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di OPM](opm-programming-reference.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> </dl>

 

 




---
description: Comandi OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandi OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119146"
---
# <a name="opm-commands"></a>Comandi OPM

Questa sezione elenca i comandi disponibili per [Output Protection Manager](output-protection-manager.md) (OPM).

Per inviare un comando OPM, chiamare [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Per ogni comando sono elencate le informazioni seguenti.



| Valore             | Descrizione                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID del comando | Identifica il comando. Impostare il **membro guidSetting** della struttura [**OPM \_ CONFIGURE \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) su questo valore. |
| Dati di input   | Specifica come interpretare la matrice **abParameters** nella [**struttura OPM \_ CONFIGURE \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                      |



 

Sono definiti i comandi seguenti:



| Comando                                                                                                       | Descrizione                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING**](opm-set-acp-and-cgmsa-signaling.md)                               | Specifica informazioni sul segnale video, diverse dal livello di protezione.                      |
| [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Aggiorna il messaggio di rinnovo del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP). |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL**](opm-set-protection-level.md)                                               | Imposta il livello di protezione per un meccanismo di protezione dell'output.                                       |
| [**OPM \_ IMPOSTA IL LIVELLO DI PROTEZIONE IN BASE AL DVD \_ \_ \_ \_ \_ \_ CSS**](opm-set-protection-level-according-to-css-dvd.md) | Imposta il livello di protezione HDCP per la riproduzione di DVD, seguendo le regole CSS (Dvd Content Scramble System). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla programmazione OPM](opm-programming-reference.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



